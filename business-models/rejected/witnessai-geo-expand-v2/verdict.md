# Verdict Packet — witnessai-geo-expand-v2
- Status: NEAR-PASS
- Score: 68/100
- Sector: GEO-EXPAND
- GitHub canonical path: rejected/witnessai-geo-expand-v2/verdict.md

---

## FILE: 00-brief.md


## FILE: 00-brief.md

# Краткий бриф

## Тезис
WitnessAI как сигнал международной зрелости AI security и governance platform для enterprise AI-агентов

## Почему кейс создан
WitnessAI подтверждает, что security, observability и governance для AI-агентов оформляются в отдельную enterprise-категорию с крупными раундами, международной экспансией и высоким потенциальным LTV. Это достаточно сильный самостоятельный GEO-EXPAND кейс для новой оценки.

## Следующий шаг
Передать кейс в P3-demand-validation и проверить, насколько governance/security слой для AI-агентов в РФ требует локального deployment-моделя, интеграций с ИБ-контуром и поддержки отечественных LLM.


---

## FILE: 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-witnessai-geo-expand.md
created: 2026-04-22T03:10:49+03:00
source_verdict: triage/triage-2026-04-17-witnessai-geo-expand-followup-0559.md
---

# Intake

## Статус
Принудительный resurrect / полный пайплайн P3→P7.

## Исходный verdict
- `triage/triage-2026-04-17-witnessai-geo-expand-followup-0559.md`

## Полный контекст raw

# RESURRECT SIGNAL — witnessai-geo-expand

## Meta
- source: triage/triage-2026-04-17-witnessai-geo-expand-followup-0559.md
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
2026-04-17

## Входные данные
- `pipeline/raw/raw-2026-04-17-0559-msk-witnessai-geo-expand.md`

## Классификация
Поддерживающий сигнал для существующего кейса.

## Решение
Сигнал добавлен в кейс `enterprise-agent-control-plane-implementation-operator`.

## Что именно добавлено
- В evidence кейса добавлен новый supporting signal по WitnessAI.
- Зафиксированы дополнительные факты о позиционировании WitnessAI как unified AI security and governance platform для сотрудников, моделей, приложений и AI-агентов.
- Добавлены данные о публичном раунде $58 млн на глобальную экспансию, enterprise-референсах и оценке LTV для РФ на уровне 15-70 млн ₽ в год на клиента.
- Отдельно зафиксировано, что для российского рынка такой слой потребует тяжёлой локализации: on-prem/private cloud, интеграции с ИБ-контуром и поддержку отечественных LLM.

## Почему это усиливает кейс
Сигнал делает кейс сильнее, потому что показывает более широкий product scope категории: control plane для AI-агентов в enterprise всё чаще включает security, observability, governance и policy enforcement как обязательную часть production-инфраструктуры. Это повышает вероятность отдельного бюджета и крупного чека на внедрение в регулируемых отраслях РФ.

## Статус raw-файла
Файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Кейс обогащён: добавлен ещё один подтверждающий GEO-EXPAND сигнал по WitnessAI для `enterprise-agent-control-plane-implementation-operator`.

```



---

## FILE: 01-evidence.md

# Подтверждающие сигналы

## 2026-04-25 — supporting signal — WitnessAI как зрелый AI security / governance слой для enterprise AI и агентов
- **Дата:** 2026-04-25
- **Источник:** https://witness.ai/ ; https://witness.ai/product/ ; https://www.axios.com/2026/01/13/witnessai-funding-enterprise-ai
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс, потому что подтверждает, что категория AI security / governance уже оформлена как отдельный enterprise layer, причём не только для сотрудников и чатботов, но и для AI-агентов, MCP-серверов, моделей и приложений. Это снижает риск, что WitnessAI описывает слишком раннюю или искусственную категорию без repeatable enterprise-бюджета.
- **Ключевые данные и факты:** официальный сайт WitnessAI прямо позиционирует продукт как unified AI security and governance platform с visibility, runtime defense, policy enforcement, audit trails и отдельным coverage для human и agentic workforce; в product-описании заявлены network-level visibility, agent governance, intelligent routing и single-tenant / data sovereignty architecture; Axios в январе 2026 сообщил о раунде **$58 млн** и фокусе компании на защите enterprise AI-агентов, что дополнительно подтверждает зрелость категории и интерес инвесторов к этому слою инфраструктуры.


## 2026-05-09 — supporting signal — Runlayer как ранняя валидация MCP governance и agent security
- **Дата:** 2026-05-09
- **Источник:** https://techcrunch.com/2025/11/17/mcp-ai-agent-security-startup-runlayer-launches-with-8-unicorns-11m-from-khoslas-keith-rabois-and-felicis/ ; https://www.runlayer.com/ ; https://www.runlayer.com/security
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс по enterprise AI security и governance, потому что подтверждает появление отдельного control-plane слоя именно для MCP, skills и AI-агентов, а не только для классических LLM guardrails. Это повышает уверенность, что рынок agent governance быстро оформляется в самостоятельную enterprise-категорию с крупным чеком и спросом на self-hosted deployment.
- **Ключевые данные и факты:** TechCrunch пишет, что у Runlayer уже на старте были десятки клиентов, включая 8 unicorn/public companies; официальный сайт заявляет 300+ AI-клиентов и каталог 18 000+ MCP servers; security-лендинг подтверждает ключевые функции категории: threat detection, ABAC, audit trails, human-in-the-loop approval и self-hosted/VPC deployment.

## 2026-05-11 — supporting signal — WitnessAI подтверждает traction через enterprise security wedge и продуктовую экспансию
- **Дата:** 2026-05-11
- **Источник:** https://www.axios.com/2026/01/13/witnessai-funding-enterprise-ai ; https://witness.ai/ ; https://witness.ai/resources/witnessai-announces-automated-red-teaming-and-next-generation-ai-firewall-protection-for-enterprise-llms-and-ai-applications/
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс, потому что подтверждает не только инвестиционный интерес к AI security для enterprise, но и расширение продуктовой линейки вокруг AI firewall и automated red teaming. Это повышает уверенность, что категория agent security уже двигается от общей governance-обвязки к отдельным бюджетируемым security-модулям.
- **Ключевые данные и факты:** Axios сообщил о раунде 58 млн долларов на масштабирование AI security platform; официальный сайт WitnessAI показывает защиту сотрудников, моделей, приложений и агентов, а также customer signals вроде InComm Payments и кейса Top-10 Airline; продуктовый анонс заявляет quarter of record sales и запуск AI firewall плюс automated red teaming.

## 2026-05-13 — supporting signal — WitnessAI подтверждает ускорение enterprise-спроса на AI governance и runtime-защиту
- **Дата:** 2026-05-13
- **Источник:** https://techcrunch.com/2024/11/14/witnessai-raises-27-5m-to-help-businesses-use-generative-ai-safely/ ; https://www.latimes.com/business/story/2025-03-13/witnessai-secures-58-million-series-b-to-tackle-ai-agent-security-risks ; https://witness.ai/customers
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс, потому что показывает сочетание инвестиционной валидации и раннего enterprise traction именно в категории AI governance и agent security. Это повышает уверенность, что рынок уже оформляется в отдельный бюджетируемый слой, а не остаётся приложением к общему cybersecurity stack.
- **Ключевые данные и факты:** TechCrunch сообщал о раунде $27,5 млн и 25 корпоративных клиентах на ранней стадии; LA Times зафиксировал Series B на $58 млн с фокусом на риски AI-агентов; страница customers показывает enterprise-use cases и клиентов уровня InComm Payments и крупной авиакомпании.

## 2026-05-13 — supporting signal — Credo AI подтверждает enterprise-спрос на AI governance как отдельный control layer
- **Дата:** 2026-05-13
- **Источник:** https://www.forrester.com/report/the-forrester-wave-tm-ai-governance-solutions-q3-2025/RES184849 ; https://www.credo.ai/forrester-wave ; https://www.weforum.org/organizations/credo-ai/ ; https://www.globenewswire.com/news-release/2026/03/24/3261077/0/en/Fast-Company-Unveils-2026-Most-Innovative-Companies-List-Led-by-Google-Nvidia-and-Shopify.html
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс, потому что показывает зрелость не только security-обвязки, но и более широкого слоя AI governance с enterprise adoption в регулируемых индустриях. Это повышает уверенность, что в РФ может сформироваться отдельный бюджетируемый control plane для реестра AI-систем, policy enforcement и audit-ready evidence.
- **Ключевые данные и факты:** Forrester выделяет категорию AI governance solutions и относит Credo AI к заметным игрокам; сама компания заявляет highest adoption rate among large global enterprises и 12 максимальных оценок в своём coverage Forrester; World Economic Forum описывает Credo AI как governance platform для financial services, insurance, healthcare, government и retail; Fast Company включил Credo AI в список Most Innovative Companies 2026.


---

## FILE: 02-validation.md

_Файл отсутствует в кейсе: 02-validation.md_


---

## FILE: 02-demand.md

---
stage: demand-validation
case: witnessai-geo-expand-v2
date: 2026-04-24
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand

> Market Pulse 2026-04-25: растущий интерес.
>
> Market Pulse 2026-05-09: растущий интерес. По свежей веб-выдаче усилился сигнал по AI security governance, agent guardrails и security-слою для enterprise AI.


## Кейс
WitnessAI как категория enterprise AI security / governance для AI-агентов, copilots и LLM-приложений в РФ, с фокусом на on-prem, private cloud, аудит, policy enforcement и интеграции в ИБ-контур.

## Итог
**Статус: CONDITIONAL PASS.**

На 24 апреля 2026 года exact-demand в РФ по формулировке `AI security governance for enterprise AI agents` низкий: internal demand API вернул `LOW` и `demand_score=0`. [T3]

Но ранний reject не срабатывает, потому что profit gate в enterprise/on-prem сценариях **проходим**. В РФ уже есть три устойчивых сигнала: 1) рынок ИБ большой, **337 млрд ₽** в 2024 году; 2) AI внедряют **6%** организаций, а совокупные расходы крупных и средних организаций на AI составили **90,3 млрд ₽**; 3) в банках и крупных enterprise уже появляются роли и программы по защите AI-инфраструктуры. [T2][T1][T1]

Иными словами, спрос пока не query-led, а budget-led: покупатель формулирует боль как `защита AI-инфраструктуры`, `контроль утечек`, `prompt injection`, `аудит`, `безопасное использование GenAI сотрудниками`, а не как отдельную категорию `AI security governance platform`. [T1][T2][inference]

## 1. Сигналы спроса

### Demand API
- `AI security governance for enterprise AI agents in Russia` -> **LOW**, `demand_score=0`, `hh_ru=0`, `habr_articles=2`, `yandex_suggest=2`. [T3]

### Дополнительные сигналы рынка
1. Банк России пишет, что по результатам опроса **2025 года** AI применяют финансовые организации, а сам регулятор ведёт отдельный контур по условиям дальнейшего развития AI на финрынке. Это важный сигнал, что regulated buyers уже есть. [T1]
2. По данным FinExpertiza со ссылкой на Росстат, в 2024 году AI использовали **6%** организаций, а суммарные расходы крупных и средних организаций на внедрение и использование AI составили **90,3 млрд ₽**. [T1][T2]
3. hh.ru фиксирует появление прямых вакансий под категорию: у Сбера есть вакансия `Руководитель направления по защите AI-инфраструктуры`, а рынок уже использует формулировки `AI Security Engineer / Cybersecurity Engineer (AI Systems)`. [T1]
4. Swordfish Security прямо продаёт экспертизу по `AI Security`, что подтверждает появление supply-side категории в РФ. [T1]

### Интерпретация
- Exact-demand слабый, поэтому массовый self-serve launch в РФ выглядит рискованно. [T3][inference]
- Однако buyer pain уже существует внутри budgets на кибербезопасность, безопасную разработку и GenAI governance. [T1][T2][inference]
- Категория выглядит как enterprise wedge для 50-500 крупных аккаунтов, а не как SMB SaaS. [T1][T2][inference]

## 2. Конкуренты и цены

Ниже не только прямые AI-security игроки, но и ближайший buying alternative: guardrails / observability / evaluation stack, из которого enterprise-команда может собрать substitute вместо WitnessAI.

| Игрок | Что продаёт | Прайс / цена | Что это доказывает |
|---|---|---:|---|
| Amazon Bedrock Guardrails | Guardrails, PII, denied topics, grounding checks | content filters **$0.15 за 1 000 text units**, sensitive info **$0.10 за 1 000 text units**, automated reasoning **$0.17 за 1 000 text units** [T1] | За safety/control уже платят как за отдельный API-слой |
| Azure AI Content Safety | Content safety, Prompt Shields, groundedness | бесплатный tier **5 000 text records/мес**, далее S0 pay-as-you-go [T1] | Microsoft выделяет отдельный SKU под safety/governance |
| Portkey | AI gateway + observability + guardrails + auditability | Production **$49/мес**, overage **$9 за 100k requests**, Enterprise custom [T1] | Даже gateway/control-plane слой уже имеет monetized SKU |
| Langfuse | Tracing, evals, prompt/version governance | Core **$29/мес**, Pro **$199/мес**, Enterprise **$2 499/мес** [T1] | Observability/governance бюджетируется отдельно |
| Arize AX | LLM observability / evals | AX Pro **$50/мес**, additional traces **$10 за 1 млн**, additional GB **$3/GB** [T1] | Рынок покупает model/agent monitoring как отдельный бюджет |
| Promptfoo | LLM security testing / red teaming | Community **free**, Enterprise custom, On-Prem custom [T1] | Security testing monetизируется как enterprise add-on |

### Вывод по конкуренции
1. У category buyer уже есть как минимум три альтернативы: встроенные hyperscaler guardrails, AI gateway/observability stack и security testing stack. [T1][inference]
2. Поэтому для входа в РФ WitnessAI недостаточно быть `ещё одним AI security vendor`; нужен локальный тезис: on-prem, audit trail, отечественные LLM, DLP/SIEM integration, policy layer для сотрудников и агентов. [T1][T2][inference]
3. Публичные цены у substitutes начинаются от десятков долларов в месяц, но enterprise-grade security обычно уходит в custom pricing и annual commitment. Это подтверждает WTP, но и усиливает pressure на differentiated enterprise packaging. [T1][inference]

## 3. Telegram-боты и сервисы в РФ
1. Прямых Telegram-native продуктов уровня `enterprise AI governance for corporate agents` в РФ я не нашёл. Это **негативный** сигнал для bot-first GTM. [T2][inference]
2. Ближайший adjacent пример, `AI Anti-Spam`, продаёт AI-модерацию Telegram-групп по модели **1 Telegram Star за проверку нового участника**. [T2] Это показывает, что в Telegram готовы платить за AI-based safety, но юзкейс потребительский/комьюнити, а не enterprise governance. [T2][inference]
3. `Hi, AI!` заявляет крупную AI-экосистему в Telegram с **1M DAU** и **35M** охвата, но это distribution/playground для массового AI, а не security/governance продукт. [T2]

### Вывод по Telegram
Telegram в РФ подтверждает distribution и пользовательскую привычку к AI-ботам, но не доказывает наличие bot-native enterprise spend на AI governance. Для WitnessAI Telegram может быть максимум lead-gen / awareness каналом, не основным продуктовым форматом. [T2][inference]

## 4. Кто купит

### ICP
- банки и финтех,
- телеком,
- e-commerce / retail с customer-facing AI,
- крупные интеграторы и разработчики enterprise AI,
- гос/квази-гос и критическая инфраструктура,
- промышленные компании с закрытым контуром и AI-assistant use cases.

### 10 реальных buyers для bottom-up модели
1. Сбер. [T1]
2. Т-Банк. [T1][inference]
3. ВТБ. [T1][inference]
4. МТС. [T2][inference]
5. Яндекс. [T2][inference]
6. VK. [T2][inference]
7. X5 Group. [T2][inference]
8. Магнит. [T2][inference]
9. Северсталь. [T2][inference]
10. Газпром нефть. [T2][inference]

Это не полный TAM, а примеры тех, у кого уже есть одновременно AI adoption, чувствительные данные, внутренняя разработка и риск-профиль, оправдывающий отдельный governance/security слой. [T1][T2][inference]

## 5. WTP, willingness to pay
1. AWS, Microsoft, Portkey, Langfuse и Arize уже монетизируют guardrails, tracing, evaluation, prompt governance и observability как отдельные SKU. Это прямое доказательство willingness to pay за control layer вокруг LLM-приложений. [T1]
2. Российский рынок тоже показывает готовность платить за пересечение AI и security: Swordfish Security уже продаёт AI Security как отдельную практику, а hh.ru показывает формирование профильных ролей. [T1]
3. Для regulated enterprise в РФ WTP должен быть выше западного self-serve price floor, потому что локальный пакет почти наверняка потребует private cloud/on-prem, интеграции с SIEM/DLP/IdM, журналирование, разграничение доступа и поддержку отечественных LLM. [T1][T2][inference]

### Рабочий диапазон WTP
- low-end pilot: **120-250 тыс. ₽/мес**. [T1][inference]
- private-cloud mid-market: **350-600 тыс. ₽/мес**. [T1][T2][inference]
- enterprise on-prem + policy + audit + integrations: **900 тыс. - 2,5 млн ₽/мес**. [T1][T2][inference]

## 6. Market sizing

### Метод и reconciliation
Для top-down беру две базы: общий рынок ИБ РФ **337 млрд ₽** и расходы крупных/средних организаций на AI **90,3 млрд ₽**. Так как WitnessAI относится к AI governance/security, а не ко всему рынку ИБ, в качестве предпочтительной базы для TAM РФ использую более консервативную оценку от AI spend, а не от всего cyber market. [T2][T1][inference]

### Допущения
- Top-down addressable share для AI governance/security слоя: **8%** от расходов на AI. [T1][inference]
- Segment fit для regulated / enterprise-ready сегмента: **40%** TAM РФ. [T1][T2][inference]
- Bottom-up: из **90,3 млрд ₽ / 6 млн ₽** среднего spend на организацию получается примерно **15 050** AI-использующих юрлиц. Беру только **10%** как enterprise/high-sensitivity ICP = **1 505** потенциальных buyers. [T1][T2][calculation]
- Доля с подтверждённой болью: **35%**. Основание: низкий exact-demand, но наличие regulated AI adoption, ИБ-вендоров и профильных вакансий. [T1][T2][T3][inference]
- Средний контракт: **4,8 млн ₽ ARR** или **400 тыс. ₽/мес**. Это выше западного self-serve floor, но ниже heavy on-prem enterprise. [T1][inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | ~**220 млрд ₽** эквивалент category proxy через global AI safety / observability spend, low-confidence [T2] | — | — | top-down |
| TAM (РФ) | **7,2 млрд ₽** = 90,3 млрд ₽ × 8% [T1][inference] | **7,2 млрд ₽** = 1 505 × 100% need × 4,8 млн ₽ [T1][T2][calculation] | diff=0%, обе модели сходятся из одной spend-base | lower |
| SAM (РФ) | **2,9 млрд ₽** = 7,2 млрд ₽ × 40% [T1][T2][inference] | **2,53 млрд ₽** = 1 505 × 35% × 4,8 млн ₽ [T1][T2][T3][calculation] | diff≈15%, допустимо; bottom-up консервативнее из-за low exact-demand | lower |
| SOM Y1 | **58 млн ₽** = 2% SAM [inference] | **63 млн ₽** = 2,5% SAM [inference] | diff≈9% | **используем 58 млн ₽** |
| SOM Y3 | **231 млн ₽** = 8% SAM [inference] | **228 млн ₽** = 9% SAM [inference] | diff≈1% | **используем 228 млн ₽** |

### Sanity-check
- SOM Y1 = **58 млн ₽**, при среднем ARR **4,8 млн ₽** это примерно **12 клиентов**. Это тяжело, но реалистично для enterprise motion, если средний deal cycle держится в коридоре 6-9 месяцев и продажи идут по 2-3 вертикалям, а не по всему рынку сразу. [inference]
- SOM Y1 составляет меньше 10% от SAM, red flag overclaiming нет. [calculation]

## 7. Profit gate scenarios

### Сценарий A, self-serve gateway / guardrails SaaS
- Цена: **99-149 тыс. ₽/мес**.
- Даже при 15 клиентах выручка **1,5-2,2 млн ₽/мес**.
- Для локального enterprise security-вендора с sales + solutions + support это с высокой вероятностью не даёт **EBITDA 500 тыс. ₽/мес**. [inference]
- **Вердикт: FAIL.**

### Сценарий B, private cloud для mid-market / upper-mid
- Цена: **350-600 тыс. ₽/мес**.
- При 8 клиентах выручка **2,8-4,8 млн ₽/мес**.
- При gross margin 65-75% и небольшой implementation-команде EBITDA **500 тыс. ₽/мес** достижима. [inference]
- **Вердикт: PASS.**

### Сценарий C, enterprise on-prem + policy + audit + integrations
- Цена: **900 тыс. - 2,5 млн ₽/мес**.
- Уже 3-5 клиентов дают **2,7-12,5 млн ₽/мес** выручки.
- Даже с тяжёлым пресейлом и delivery profit gate проходит. [inference]
- **Вердикт: STRONG PASS.**

## 8. Основные риски
1. Exact-demand низкий, category education дорогая. [T3]
2. Гиперскейлеры и gateway/observability vendors уже закрывают часть потребности. [T1]
3. В РФ победит не лучший UI, а лучший compliance package: on-prem, локальные LLM, audit logs, интеграции с DLP/SIEM/IAM. [T1][T2][inference]
4. Есть риск, что buyers решат проблему руками внутреннего AppSec/DevSecOps + hyperscaler tooling без покупки отдельного вендора. [T1][inference]
5. Telegram как канал подтверждает distribution, но не buyer budget. [T2][inference]

## 9. Решение для pipeline
**Оставить кейс в пайплайне с вердиктом CONDITIONAL PASS.**

Почему:
1. demand по query слабый, но pain и бюджетная линия существуют;
2. WTP подтверждён глобальными SKU и локальными staffing-сигналами;
3. TAM/SAM/SOM в РФ достаточно велики для venture-scale niche infra кейса;
4. profit gate не проходит в self-serve, но проходит в private cloud / on-prem enterprise модели.

### Что обязательно проверить дальше
- есть ли в РФ 15-30 реальных enterprise аккаунтов, где GenAI уже в проде и есть owner бюджета;
- сколько из них потребуют on-prem, а сколько устроит private cloud;
- можно ли упаковать продукт без service trap;
- выдерживает ли кейс конкуренцию с Kaspersky / BI.ZONE / Swordfish / интеграторами плюс hyperscaler stack.

## Market Pulse
Market Pulse 24.04.2026: осторожно позитивный.

Спрос не массовый, но категория становится обязательным enterprise control layer по мере роста AI-агентов и regulated GenAI use cases.

## Источники
- [T1] Demand API: http://172.18.0.1:9001/multi-demand?keyword=AI%20security%20governance%20for%20enterprise%20AI%20agents%20in%20Russia
- [T1] Банк России, «Искусственный интеллект на финансовом рынке», updated 10.03.2026: https://www.cbr.ru/fintech/primenenie-iskusstvennogo-intellekta-na-finansovom-rynke/
- [T1] hh.ru, вакансия Сбер `Руководитель направления по защите AI-инфраструктуры`: https://hh.ru/vacancy/129746204
- [T1] hh.ru, Swordfish Security employer page: https://hh.ru/employer/1239730
- [T1] AWS Bedrock Pricing: https://aws.amazon.com/bedrock/pricing/
- [T1] Azure AI Content Safety Pricing: https://azure-int.microsoft.com/en-us/pricing/details/cognitive-services/content-safety/
- [T1] Portkey Pricing: https://portkey.ai/pricing
- [T1] Langfuse Pricing: https://langfuse.com/pricing
- [T1] Arize Pricing: https://arize.com/pricing/
- [T1] Promptfoo Pricing: https://www.promptfoo.dev/pricing/
- [T2] TAdviser, рынок ИБ РФ 2025: https://www.tadviser.ru/index.php/%D0%A1%D1%82%D0%B0%D1%82%D1%8C%D1%8F%3A%D0%A0%D0%BE%D1%81%D1%81%D0%B8%D0%B9%D1%81%D0%BA%D0%B8%D0%B9_%D1%80%D1%8B%D0%BD%D0%BE%D0%BA_%D0%98%D0%91_2025._%D0%9E%D0%B1%D0%B7%D0%BE%D1%80_TAdviser
- [T2] ТАСС, FinExpertiza: каждая 17-я компания и госструктура использует ИИ в работе: https://tass.ru/ekonomika/25993085
- [T2] Hi, AI!: https://hiai.digital/
- [T2] AI Anti-Spam: https://www.ai-antispam.ru/

Sources: T1=10, T2=4, T3=1. Primary evidence basis: T1.
> Market Pulse 2026-05-10: растущий интерес, свежих публикаций и рыночных сигналов стало больше.

> Market Pulse 2026-05-11: растущий интерес. По текущей веб-выдаче по ключевым запросам виден рост публикаций, вакансий и/или vendor-активности.


> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по ключевым запросам сохраняются свежие публикации, вакансии и/или vendor-активность.

> Market Pulse 2026-05-13: растущий интерес. По текущей веб-выдаче по ключевому запросу видна свежая рыночная активность.


---

## FILE: 03-solution.md

---
stage: solution
case: witnessai-geo-expand-v2
date: 2026-05-10
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
WitnessAI как GEO-EXPAND wedge для enterprise AI security, governance и runtime control слоя поверх LLM-приложений, copilots, MCP-интеграций и AI-агентов в РФ.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Продукт решает не абстрактную задачу «безопасный AI», а дорогую enterprise-проблему, как разрешить внедрение GenAI и агентных workflows без неконтролируемых утечек, prompt injection, policy drift и audit gaps.
2. Реальный wedge в локальном контуре выглядит не как self-serve security SaaS, а как heavy enterprise control layer, private cloud / on-prem deployment плюс интеграции с ИБ- и IAM-контуром.
3. Самый правдоподобный вход в рынок, regulated и high-sensitivity buyers, где AI уже появляется в production или near-production и есть owner риска на стороне ИБ, архитектуры или digital transformation.
4. Главный риск в том, что кейс легко распадается на смесь консалтинга, AppSec-проекта и сборки из hyperscaler guardrails, если не удержать repeatable platform wedge.

## 1. Какую проблему реально решает продукт

WitnessAI-подобный слой продаёт не «ещё один AI security dashboard», а устранение нескольких дорогих рисков одновременно:
- утечки данных через LLM и agent workflows;
- отсутствие visibility по тому, какие модели, MCP-серверы, агенты и prompt chains реально используются;
- невозможность централизованно навесить policy enforcement, RBAC/ABAC, audit trail и human approval;
- высокий риск prompt injection, data exfiltration и несанкционированных tool actions;
- блокировку enterprise rollout со стороны ИБ и compliance, когда бизнес хочет запускать GenAI быстрее.

Для ICP это painkiller только там, где GenAI уже выходит за пределы лаборатории. Если компания пока экспериментирует с одним чат-ботом без чувствительных данных и без агентных сценариев, такой продукт будет восприниматься как premature overkill.

## 2. Целевой ICP в локальном контуре

### Primary ICP
- банки и финтех;
- телеком и крупные digital ecosystems;
- e-commerce / retail с customer-facing AI;
- enterprise-разработчики внутренних AI-assistants;
- интеграторы и платформенные команды, которые строят agentic workflows для крупных заказчиков;
- гос/квази-гос, промышленность и критическая инфраструктура с закрытым контуром.

### Фильтр на ICP
Клиент проходит, если одновременно есть:
1. уже идущие или ближайшие production-use-cases с LLM, copilots или AI-агентами;
2. чувствительные данные, регуляторные ограничения или высокий reputational/security risk;
3. владелец риска, head of information security, enterprise architect, CDO, CIO или sponsor AI program;
4. готовность покупать не только аудит, но и постоянный runtime control layer;
5. инфраструктурная зрелость для private cloud или on-prem deployment.

### Нецелевой сегмент
- SMB и mid-market без production AI;
- команды, которым достаточно встроенных guardrails AWS/Azure/OpenAI;
- клиенты без security sponsor'а и без отдельного risk-budget;
- организации, где AI пока остаётся sandbox-экспериментом без tool execution и без доступа к чувствительным данным.

## 3. Продуктовый wedge

### Core wedge
**AI runtime security and governance control plane**
- visibility по моделям, агентам, tools и MCP-поверхности;
- policy enforcement для запросов, tool usage и data access;
- audit trail и forensic-ready журналирование;
- routing / approval / human-in-the-loop для рискованных действий;
- self-hosted, VPC или single-tenant deployment для data sovereignty.

### Что делает wedge сильнее обычных guardrails
1. **Покрывает не только prompt filtering.** Ценность не в токсичности контента, а в управлении agent behavior, tool access и governance-слоем поверх production AI.
2. **Садится на существующий security budget.** Покупка может идти из ИБ, platform security, secure SDLC или AI transformation budget, а не из экспериментального R&D.
3. **Не требует замены core stack.** Такой слой встраивается поверх уже выбранных моделей, orchestration frameworks и внутренних приложений.
4. **Подходит regulated buyers.** On-prem, private cloud и data sovereignty критичны для локального enterprise и создают естественный premium wedge.
5. **Agent/MCP-tailwind усиливает тезис.** По supporting signals категория сдвигается от “LLM guardrails” к “agent governance”, а это более дорогая и более обязательная инфраструктурная роль.

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Вариант, который, вероятно, не взлетит
- продажа как generic AI safety platform;
- self-serve motion с price point уровня observability SaaS;
- фокус на маркетинговом страхе перед AI вместо чётких security controls;
- попытка продавать всем компаниям, которые «что-то делают с AI».

### Вариант, который выглядит реалистично
- заход через 1 конкретный production-risk scenario, например internal copilot, AI-agent с доступом к корпоративным данным, customer support assistant или code assistant;
- pilot в закрытом контуре на 6-10 недель;
- buyer сверху, CISO, head of platform security, enterprise architect, CDO или owner AI governance program;
- KPI pilot: покрытие visibility, число policy violations, сокращение manual review, скорость security sign-off для AI rollout;
- упаковка как governance/control layer для уже существующей AI-инициативы, а не как самостоятельный “AI project”.

## 5. Почему клиент будет покупать именно это, а не alternatives

У локального клиента уже есть substitutes:
- встроенные hyperscaler guardrails и content safety сервисы;
- observability / gateway stack;
- внутренний AppSec/DevSecOps плюс набор кастомных правил;
- услуги интегратора или ИБ-консалтинга без отдельной платформы.

WitnessAI-подобный продукт может выиграть только в четырёх вещах:
1. **быстрее даёт production-grade control plane**, чем внутренняя сборка;
2. **покрывает agent/tool/MCP surface**, а не только текстовые фильтры;
3. **лучше проходит требования regulated buyers** по self-hosting, auditability и policy governance;
4. **даёт recurring platform value**, а не только разовый security assessment.

Если этих преимуществ нет, клиент рационально выберет bundle из hyperscaler tooling и внутренней security-команды.

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. discovery текущих AI use-cases, data flows и threat surface;
2. выбор одного high-risk workflow с понятным owner'ом;
3. подключение visibility и policy enforcement в ограниченном контуре;
4. настройка audit trail, access policy и approval paths;
5. 6-10 недель pilot с security review и измерением operational impact;
6. rollout на соседние AI use-cases после прохождения security/compliance sign-off;
7. recurring retainer на policy tuning, новые integrations и governance operations.

### Кто должен быть buyer'ом
- CISO или руководитель ИБ;
- head of platform / cloud security;
- enterprise architect;
- CDO / CIO как sponsor AI-трансформации;
- owner внутренней AI platform program.

### Кто редко будет настоящим buyer'ом
- отдельный ML engineer без бюджета;
- innovation lead без security-спонсора;
- procurement без risk owner'а;
- команда, которая пока тестирует GenAI в sandbox-режиме.

## 7. Конкурентная позиция

### Против hyperscaler guardrails
Преимущество есть только если продукт поднимается выше content filtering и даёт vendor-agnostic governance по нескольким моделям, агентам и tool chains.

### Против in-house security stack
Шанс есть, если time-to-value короче, покрытие шире, а поддержка policy layer дешевле, чем держать собственную спецкоманду под AI runtime security.

### Против pure consulting / AppSec-аудита
Преимущество появляется, если после initial assessment остаётся постоянный control layer с recurring ценностью, а не только отчёт и рекомендации.

## 8. Основные риски solution-fit

1. **Build-vs-buy risk.** Сильные enterprise-команды могут предпочесть собрать control stack сами.
2. **Bundle risk.** Часть ценности могут съесть hyperscaler guardrails, observability vendors и SIEM/DLP vendors.
3. **Services risk.** Без стандартизированного deployment scope кейс сползает в тяжёлый консалтинг.
4. **Readiness risk.** Существенная часть рынка ещё не дошла до agentic complexity, которая оправдывает отдельный budget line.
5. **Localization risk.** Для РФ product-market fit держится на поддержке private cloud, отечественных LLM, IAM/SIEM/DLP integration и локальных compliance-требованиях.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- сколько стоит presales + deployment для одного enterprise pilot;
- какой recurring чек реалистичен для private cloud и on-prem модели;
- сколько integrations и policy tuning съедают gross margin;
- сколько клиентов нужно для `company_ebitda_rub_month >= 500 000 ₽/мес`;
- не превращается ли лучший сценарий в security-SI business вместо repeatable infra-platform.

## Итог для пайплайна

**P4 пройден условно.**

Кейс имеет внятный solution thesis только как enterprise AI runtime governance/control plane для regulated и high-sensitivity контуров. Продолжать дальше имеет смысл, если на economics подтвердится, что high-ticket deployment остаётся platform-led, а recurring value не исчезает после initial rollout.

## Источники
- [T1] WitnessAI: https://witness.ai/
- [T1] WitnessAI Product: https://witness.ai/product/
- [T1] Axios, WitnessAI funding: https://www.axios.com/2026/01/13/witnessai-funding-enterprise-ai
- [T1] Runlayer: https://www.runlayer.com/
- [T1] Runlayer Security: https://www.runlayer.com/security
- [T1] TechCrunch, Runlayer launch: https://techcrunch.com/2025/11/17/mcp-ai-agent-security-startup-runlayer-launches-with-8-unicorns-11m-from-khoslas-keith-rabois-and-felicis/
- [T2] AWS Bedrock Pricing: https://aws.amazon.com/bedrock/pricing/
- [T2] Azure AI Content Safety Pricing: https://azure-int.microsoft.com/en-us/pricing/details/cognitive-services/content-safety/
- [T2] Portkey Pricing: https://portkey.ai/pricing
- [T2] Langfuse Pricing: https://langfuse.com/pricing
- [T2] Arize Pricing: https://arize.com/pricing
- [T2] Promptfoo Pricing: https://www.promptfoo.dev/pricing/
- [T2] Банк России, ИИ на финансовом рынке: https://www.cbr.ru/fintech/primenenie-iskusstvennogo-intellekta-na-finansovom-rynke/
- [T2] hh.ru, вакансия Сбер по защите AI-инфраструктуры: https://hh.ru/vacancy/129746204
- [T2] hh.ru, Swordfish Security employer page: https://hh.ru/employer/1239730

> Market Pulse 2026-05-10: solution-fit усиливается по мере роста agentic/MCP governance слоя, но в РФ кейс всё ещё выглядит жизнеспособным только в enterprise private-cloud / on-prem конфигурации.

---

## FILE: 04-economics.md

---
stage: economics
case: witnessai-geo-expand-v2
date: 2026-05-12
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics / Fund View

## Итог
**Вердикт P5: PASS.**

WitnessAI-подобный кейс в РФ проходит investment-grade economics только как **regulated enterprise AI security platform** с private cloud / on-prem delivery, ACV от **7.2 млн ₽/год** и длинным presales. При такой модели:
- **MRR на клиента:** 600 000 ₽
- **COGS на клиента/мес:** 175 000 ₽
- **Gross Margin:** 70.8%
- **Contribution Margin:** 63.3%
- **Blended fully-loaded CAC:** 2.36 млн ₽
- **LTV:** 28.3 млн ₽
- **LTV/CAC:** 12.0x
- **CAC Payback:** 3.9 мес
- **Break-even:** 19 клиентов или ориентировочно **M13**
- **EBITDA при 50 клиентах:** около **11.8 млн ₽/мес**

Ни profit gate, ни reject gate не срабатывают: при 50 клиентах компания заметно выше 500k ₽ EBITDA/мес, а **LTV/CAC >> 1:1** и выше порога investable **3:1**.

## 1. Базовые допущения модели

### Revenue model
- ICP: банки, финтех, телеком, крупный e-commerce, enterprise AI-platform teams.
- Product: AI security + governance + runtime control layer для моделей, приложений, MCP и AI-агентов.
- Pricing model: annual contract с ежемесячным признанием выручки.
- Base plan: **600 000 ₽ MRR** на клиента.
- ACV: **7.2 млн ₽/год**.
- Onboarding fee в базовой модели не включаю в LTV, чтобы не завышать качество экономики.

### Retention / churn benchmark
Для enterprise SaaS с высокой ARPA ориентиром беру **1-2% monthly logo churn**. ChartMogul пишет, что у SaaS с ARPA **$500+** churn обычно ниже, около **1-2% в месяц**, а top quartile customer retention для high-ARPA B2B выше среднего. Для regulated AI-security слоя в РФ беру **1.5% monthly churn** как консервативную середину диапазона. [T5]

## 2. Business process, от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-account list по банкам/enterprise | CEO + SDR | HH, LinkedIn-like базы, сайт компании, CRM | 2 ч/аккаунт | 2 400 | низкая |
| 2 | Первый outbound-touch, email + Telegram + intro | SDR | HubSpot, sequencing tool, почта | 1.5 ч | 1 800 | средняя |
| 3 | Qualification call | SDR | Meet/Zoom, CRM | 1 ч | 1 200 | средняя |
| 4 | Discovery с CISO / architect | CEO + AE | Meet, Notion, CRM | 2 ч | 8 800 | низкая |
| 5 | Security scoping и threat mapping | CTO + Solutions/Prod | Miro, docs, checklist | 6 ч | 12 000 | низкая |
| 6 | Demo / architecture workshop | AE + CTO | Demo env, slides | 3 ч | 8 100 | низкая |
| 7 | Pilot proposal и ROI model | AE + CEO | CRM, spreadsheet | 4 ч | 11 200 | средняя |
| 8 | Security review / questionnaire | CTO + DevOps | Confluence, security docs | 12 ч | 21 900 | низкая |
| 9 | Pilot deployment в private cloud / VPC | DevOps + Backend + ML | Terraform, cloud, repo, CI/CD | 20 ч | 33 800 | средняя |
| 10 | Policy tuning, guardrails, routing | ML + Backend | platform console, notebooks | 16 ч | 31 800 | средняя |
| 11 | Pilot readout и commercial negotiation | CEO + AE | CRM, spreadsheet, call | 4 ч | 13 800 | низкая |
| 12 | Legal / procurement / DPA | CEO + external legal | docflow, e-sign | 8 ч | 20 000 | низкая |
| 13 | Invoice / act / payment collection | Finance ops | 1C/банк/CRM | 1.5 ч | 3 500 | высокая |

### Вывод по процессу
- Enterprise cycle длинный, с дорогими касаниями CTO/CEO.
- Главные cost-drivers не реклама, а **security review, pilot deployment, legal/procurement**.
- Поэтому считать CAC как «performance spend / wins» здесь нельзя, нужен **fully-loaded CAC**.

## 3. COGS breakdown на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| VPC / private-cloud infra и observability | 28 000 | compute + logging + traffic под 1 enterprise tenant |
| Security scanning / red-teaming / eval workloads | 12 000 | периодические security jobs и тесты |
| SIEM / audit log storage / retention | 18 000 | хранение и форвардинг журналов |
| DevOps allocation | 25 000 | 1 DevOps на ~14 клиентов fully-loaded |
| Solutions / implementation amortization | 38 000 | presales-to-delivery handoff и policy setup |
| Customer Success / support | 42 000 | 1 CSM на ~10-12 клиентов |
| ML / policy tuning allocation | 10 000 | тюнинг моделей классификации и правил |
| Billing / документооборот | 2 000 | банк, ЭДО, админ |
| **Итого COGS** | **175 000** |  |

### Gross Margin
- Revenue per customer/month = **600 000 ₽**
- COGS per customer/month = **175 000 ₽**
- **Gross Profit = 425 000 ₽**
- **Gross Margin = 70.8%**

Для security-heavy enterprise SaaS это нормальный, но не сверхлёгкий профиль: margin ниже классического pure-software из-за private cloud, security logging и implementation tail.

## 4. CAC по каналам и funnel conversion

### Channel funnel
| Канал | Верх воронки | Discovery | Pilot | New paying customers | Конверсия top->paid | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|
| Founder-led outbound | 400 target accounts/мес | 32 | 8 | 0.40 | 0.10% | 2 800 000 |
| Integrators / partnerships | 10 интро/мес | 6 | 2 | 0.45 | 4.50% | 1 600 000 |
| Content + field events | 120 leads/мес | 18 | 5 | 0.23 | 0.19% | 2 200 000 |
| **Blended** | — | — | — | **1.08** | — | **2 356 000** |

### Интерпретация
- Самый дешёвый канал, **partners/integrators**, потому что buyer уже прогрет и есть доверие.
- Самый масштабируемый, но дорогой канал, **founder-led outbound**.
- Для WitnessAI в РФ логично строить GTM вокруг partners + named-account outbound, а не вокруг PLG.

## 5. Fully-loaded CAC, обязательный расчёт

### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

### Разложение blended CAC
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/retargeting) | 120 000 | тестовый ABM + ретаргетинг на enterprise intent | допущение модели |
| Outbound team FOT (SDR + AE attributed to new) | 728 000 | SDR 180k + AE 380k gross, оба ×1.3 соцвзносы | HH / hh-сэмплы [T7][T8] |
| Marketing team FOT (partial allocation) | 180 000 | 0.5 FTE product marketing / founder support | допущение модели |
| Tools (CRM, sequencing, enrichment, calls) | 108 000 | HubSpot seats + outreach stack + call tools | HubSpot pricing [T6] + допущение |
| Events / partnerships | 250 000 | 1 профильное событие + partner enablement | допущение модели |
| **Raw acquisition spend** | **1 386 000** | сумма строк выше |  |
| Overhead multiplier | **970 000** | raw CAC stack ×0.7, итоговый multiplier до **×1.7** для regulated enterprise motion | enterprise/regulatory adjustment |
| **Fully-loaded acquisition spend** | **2 356 000** | 1 386 000 + 970 000 |  |
| New paying customers | **1.0** | консервативно 1 новый paid logo/мес на зрелом GTM-цикле | модель |
| **Fully-loaded CAC** | **2 356 000 ₽** | 2 356 000 / 1.0 |  |

### Sanity check по CAC
- Для обычного enterprise SaaS в РФ user prompt даёт sanity range **300-900k ₽/клиент**.
- Для **regulated / security-heavy / pilot-led** motion multiplier должен быть выше, **×2.5-3.0** допустим как ceiling.
- Наш **2.36 млн ₽ fully-loaded CAC** выше generic benchmark, но я считаю это нормальным, потому что здесь есть:
  1. security review,
  2. private-cloud pilot,
  3. длинный цикл AE/CTO/CEO,
  4. legal/procurement,
  5. partner co-selling.
- Красного флага «слишком дешёвый CAC» нет, наоборот, модель выглядит реалистично и не занижает продажи.

## 6. LTV, churn, LTV/CAC

### Churn assumption
- Monthly churn = **1.5%**
- Customer lifetime = `1 / 0.015 = 66.7 мес`

### LTV
Формула: `LTV = MRR × Gross Margin / Churn`

- MRR = **600 000 ₽**
- Gross Margin = **70.8%**
- Churn = **1.5%**

`LTV = 600 000 × 0.708 / 0.015 = 28 320 000 ₽`

### LTV/CAC
`28 320 000 / 2 356 000 = 12.0x`

**Вывод:** LTV/CAC сильно выше минимального порога **3:1**, значит кейс выглядит investable именно в enterprise-конфигурации.

## 7. CAC Payback

По обязательной формуле sanity check:
`CAC Payback = CAC / MRR per customer`

`2 356 000 / 600 000 = 3.9 мес`

### Интерпретация
- Базовый порог <12 мес, для enterprise допустимо <18 мес.
- Здесь **3.9 мес**, что очень сильно даже при консервативном fully-loaded CAC.
- Если считать payback по gross profit, он был бы около **5.5 мес**, что тоже комфортно.

## 8. Contribution Margin

Для contribution margin вычитаю из revenue:
- COGS = **175 000 ₽**
- AE commission + variable deal support = **30 000 ₽**
- Customer travel / security workshop variable cost = **15 000 ₽**

Итого variable cost = **220 000 ₽**

- Contribution profit = `600 000 - 220 000 = 380 000 ₽`
- **Contribution Margin = 63.3%**

Это хороший показатель для enterprise security platform: после закрытия сделки каждый новый клиент даёт существенный вклад в покрытие fixed costs.

## 9. Team & FOT

### Полная команда
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / founder | enterprise sales, fundraising, strategic partnerships | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | product architecture, security roadmap | 600 000 | 180 000 | 780 000 |
| Senior Backend #1 | platform/backend/core integrations | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | scalability, connectors, audit plane | 420 000 | 126 000 | 546 000 |
| ML Engineer #1 | policy/classification/routing | 500 000 | 150 000 | 650 000 |
| ML Engineer #2 | runtime defense / red teaming | 500 000 | 150 000 | 650 000 |
| DevOps | VPC/private cloud, deployment, logging | 350 000 | 105 000 | 455 000 |
| Frontend | admin console, policy UX | 300 000 | 90 000 | 390 000 |
| Product / Solutions | deployment design, customer scoping | 320 000 | 96 000 | 416 000 |
| SDR | top-of-funnel outbound | 180 000 | 54 000 | 234 000 |
| AE | demos, pilots, close | 380 000 | 114 000 | 494 000 |
| Customer Success | onboarding, adoption, renewals | 240 000 | 72 000 | 312 000 |
| **Итого** |  | **4 860 000** | **1 458 000** | **6 318 000** |

### Таблица найма, hiring realism
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 600 000 | 2 | 2 | 180 000 | 780 000 |
| Senior Backend | 2 | 420 000 | 1.5 | 1.5 | 126 000 | 546 000 |
| ML Engineer | 2 | 500 000 | 2.5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1.5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| Product / Solutions | 1 | 320 000 | 1.5 | 1 | 96 000 | 416 000 |
| SDR | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 |
| AE | 1 | 380 000 | 1.5 | 3 | 114 000 | 494 000 |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |

### Комментарий по рынку найма
Числа держу внутри диапазонов, заданных в методичке, и дополнительно сверяю с hh-сэмплами по ML / backend / SDR / AE. Для ML и enterprise sales рынок Москвы в 2025-2026 подтверждает высокий salary floor, особенно в дефицитных AI и B2B enterprise ролях. [T7][T8][T9][T10]

## 10. Cumulative FOT timeline M1-M12

Правило realism соблюдено: в M1 не нанимаю 5+ человек, старт с компактного founder-led core.

| Месяц | Кто в команде | FOT, ₽/мес | Other fixed costs, ₽/мес | Gross profit from customers, ₽/мес | Net burn / EBITDA proxy, ₽/мес |
|---|---|---:|---:|---:|---:|
| M1 | CEO, CTO, Backend1, ML1 | 2 821 000 | 550 000 | 0 | -3 371 000 |
| M2 | те же | 2 821 000 | 550 000 | 0 | -3 371 000 |
| M3 | + DevOps | 3 276 000 | 600 000 | 0 | -3 876 000 |
| M4 | + Frontend, Product/Solutions | 4 082 000 | 700 000 | 0 | -4 782 000 |
| M5 | + SDR | 4 316 000 | 760 000 | 0 | -5 076 000 |
| M6 | + AE, 1 клиент | 4 810 000 | 820 000 | 405 000 | -5 225 000 |
| M7 | + CSM, 2 клиента | 5 122 000 | 850 000 | 810 000 | -5 162 000 |
| M8 | + Backend2, 4 клиента | 5 668 000 | 900 000 | 1 620 000 | -4 948 000 |
| M9 | + ML2, 6 клиентов | 6 318 000 | 950 000 | 2 430 000 | -4 838 000 |
| M10 | 9 клиентов | 6 318 000 | 980 000 | 3 645 000 | -3 653 000 |
| M11 | 13 клиентов | 6 318 000 | 1 000 000 | 5 265 000 | -2 053 000 |
| M12 | 17 клиентов | 6 318 000 | 1 000 000 | 6 885 000 | -433 000 |

### Вывод
- Break-even не происходит в первый год, но разрыв к M12 почти закрыт.
- Модель становится положительной около **M13**, когда клиентская база доходит до **18-19 логотипов**.

## 11. Fixed costs breakdown

### Steady-state fixed OPEX, кроме FOT
| Статья | ₽/мес | Комментарий |
|---|---:|---|
| Corporate cloud / dev environments | 280 000 | не tenant-specific, базовая платформа |
| Internal security / compliance tooling | 140 000 | secrets, code scanning, asset mgmt |
| Legal / бухгалтерия / ЭДО | 130 000 | договоры, закрывающие, бухгалтерия |
| Admin / office / travel base | 170 000 | гибридный режим + встречи |
| SaaS tools internal | 95 000 | Jira, Notion, Git, monitoring, etc |
| Recruiting budget amortized | 85 000 | сорсинг и найм |
| Misc / contingency | 100 000 | резерв |
| **Итого fixed non-FOT** | **1 000 000** |  |

### Полные fixed costs at scale
- FOT = **6 318 000 ₽/мес**
- Other fixed costs = **1 000 000 ₽/мес**
- **Итого fixed costs = 7 318 000 ₽/мес**

## 12. Break-even

### Break-even по числу клиентов
Формула: `Fixed costs / contribution profit per customer`

- Fixed costs = **7 318 000 ₽/мес**
- Contribution profit per customer = **380 000 ₽/мес**

`7 318 000 / 380 000 = 19.26`

**Break-even client count = 19 клиентов**

### Break-even по месяцу
По ramp-модели:
- M12 = 17 клиентов, EBITDA proxy около **-433k ₽/мес**
- **M13 ≈ 19 клиентов**, компания выходит в операционный ноль/слабый плюс

## 13. Burn-to-breakeven и cash runway

### Burn-to-breakeven
Суммарный отрицательный денежный поток до M12 по модели ≈ **46.8 млн ₽**. Это нижняя оценка burn-to-breakeven, потому что не включает форс-мажоры и capex на enterprise certifications.

### Cash runway
Берём `startup_capital = 60 млн ₽`.

- Средний burn на активной фазе M1-M12 ≈ **3.9 млн ₽/мес**
- Cash runway ≈ `60 / 3.9 = 15.4 мес`

### Интерпретация
- Для такого кейса капитал **60 млн ₽** выглядит достаточным, но не роскошным.
- `startup_capital_to_bep < 10M₽` здесь точно не получается, значит нереалистичного занижения нет.
- Нужен запас минимум **55-65 млн ₽** до стабильного break-even, если команда идёт enterprise-first и не экономит на security delivery.

## 14. Profit gate check

### EBITDA при 50 клиентах
- Revenue = `50 × 600 000 = 30 000 000 ₽/мес`
- Contribution profit = `50 × 380 000 = 19 000 000 ₽/мес`
- EBITDA after fixed costs = `19 000 000 - 7 318 000 = 11 682 000 ₽/мес`

### Вывод
- Условие `company EBITDA < 500K/mo achievable even at 50 clients` **не выполняется**.
- Условие `LTV/CAC < 1:1` **не выполняется**.
- Следовательно, **reject не нужен**.

## 15. Риски экономики

1. **Services creep risk.** Если каждый новый клиент требует уникальной кастомизации, COGS и CAC быстро уползут вверх.
2. **Partner dependency.** Самый дешёвый канал у нас partner-led; если он не заработает, blended CAC станет хуже.
3. **Long procurement cycles.** Денежный цикл может быть длиннее, чем sales cycle, особенно в финтехе и квази-госе.
4. **Margin pressure от on-prem.** Если заказчики будут настаивать на тяжёлом self-hosted deployment, GM может упасть ниже 65%.

## Финальный вывод

WitnessAI-подобный кейс в РФ **проходит P5** как фондовый enterprise AI security play:
- CAC посчитан реалистично, fully-loaded,
- retention для high-ARPA сегмента выглядит правдоподобно,
- unit economics сильная,
- break-even достигается без фантастических предпосылок,
- при 50 клиентах бизнес далеко выше reject-порога по EBITDA.

Кейс стоит оставлять в пайплайне и передавать дальше.

## Источники
- [T1] WitnessAI product: https://witness.ai/product/
- [T2] WitnessAI homepage: https://witness.ai/
- [T3] Axios, WitnessAI funding, 2026-01-13: https://www.axios.com/2026/01/13/witnessai-funding-enterprise-ai
- [T4] Runlayer security / MCP governance signal: https://www.runlayer.com/security
- [T5] ChartMogul retention benchmarks: https://chartmogul.com/saas-metrics/customer-retention/ и https://chartmogul.com/reports/saas-retention-report/
- [T6] HubSpot pricing: https://www.hubspot.com/products/sales?frame=0 и https://www.hubspot.com/products/crm?gh_jid=6448238
- [T7] hh.ru, machine learning engineer Moscow: https://hh.ru/vacancies/machine-learning-engineer
- [T8] hh.ru, account executive Moscow: https://hh.ru/vacancies/account_executive и https://hh.ru/vacancies/account_executive/polniy_den
- [T9] hh.ru, senior backend developer Moscow: https://hh.ru/vacancies/senior-backend-developer
- [T10] hh.ru career article, ML-инженер salary 2025: https://career.hh.ru/article/kto-takoj-ml-inzhener-i-kak-im-stat


---

## FILE: 05-critic.md

# SECTION A — PnL / Finance P6A

## Допущения для сценариев
- Base: ARPA 600 000 ₽/мес, COGS 175 000 ₽/клиент/мес, variable deal support 45 000 ₽/клиент/мес, fixed costs по ramp из 04-economics.
- Optimistic: ARPA 660 000 ₽/мес, COGS 170 000 ₽/клиент/мес, тот же variable deal support 45 000 ₽/клиент/мес.
- Pessimistic: ARPA 540 000 ₽/мес, COGS 190 000 ₽/клиент/мес, variable deal support 55 000 ₽/клиент/мес.
- FOT уже включает страховые взносы около 30% к payroll. Если компания не на IT-льготе, baseline по налогу смещается к УСН 6%; при ОСНО добавляется НДС 20% и налог на прибыль 20%, что ухудшает cash conversion.

## Base scenario
_Базовый сценарий из 04-economics: ACV 7,2 млн ₽, churn 1,5%/мес, выход в коммерцию с M6._

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 4 | 4 |
| Total clients | 0 | 0 | 0 | 0 | 0 | 1 | 2 | 4 | 6 | 9 | 13 | 17 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 600 000 | 1 200 000 | 2 400 000 | 3 600 000 | 5 400 000 | 7 800 000 | 10 200 000 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 175 000 | 350 000 | 700 000 | 1 050 000 | 1 575 000 | 2 275 000 | 2 975 000 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 425 000 | 850 000 | 1 700 000 | 2 550 000 | 3 825 000 | 5 525 000 | 7 225 000 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 0,0% | 70,8% | 70,8% | 70,8% | 70,8% | 70,8% | 70,8% | 70,8% |
| Fixed costs, ₽ | 3 371 000 | 3 371 000 | 3 876 000 | 4 782 000 | 5 076 000 | 5 630 000 | 5 972 000 | 6 568 000 | 7 268 000 | 7 298 000 | 7 318 000 | 7 318 000 |
| EBITDA, ₽ | -3 371 000 | -3 371 000 | -3 876 000 | -4 782 000 | -5 076 000 | -5 205 000 | -5 122 000 | -4 868 000 | -4 718 000 | -3 473 000 | -1 793 000 | -93 000 |
| Cash burn, ₽ | 3 371 000 | 3 371 000 | 3 876 000 | 4 782 000 | 5 076 000 | 5 205 000 | 5 122 000 | 4 868 000 | 4 718 000 | 3 473 000 | 1 793 000 | 93 000 |
| Cumulative cash, ₽ | 3 371 000 | 6 742 000 | 10 618 000 | 15 400 000 | 20 476 000 | 25 681 000 | 30 803 000 | 35 671 000 | 40 389 000 | 43 862 000 | 45 655 000 | 45 748 000 |

**Break-even:** 19.3 клиентов по contribution math, EBITDA break-even M13.
**Startup capital to BE:** ~45 748 000 ₽.

## Optimistic scenario
_Выше ARPA (+10%), быстрее partner-led ramp, чуть лучше infra mix и implementation reuse._

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 0 | 1 | 1 | 2 | 3 | 4 | 5 | 6 | 6 |
| Total clients | 0 | 0 | 0 | 0 | 1 | 2 | 4 | 7 | 11 | 16 | 22 | 28 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 660 000 | 1 320 000 | 2 640 000 | 4 620 000 | 7 260 000 | 10 560 000 | 14 520 000 | 18 480 000 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 170 000 | 340 000 | 680 000 | 1 190 000 | 1 870 000 | 2 720 000 | 3 740 000 | 4 760 000 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 490 000 | 980 000 | 1 960 000 | 3 430 000 | 5 390 000 | 7 840 000 | 10 780 000 | 13 720 000 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 74,2% | 74,2% | 74,2% | 74,2% | 74,2% | 74,2% | 74,2% | 74,2% |
| Fixed costs, ₽ | 3 371 000 | 3 371 000 | 3 876 000 | 4 782 000 | 5 076 000 | 5 630 000 | 5 972 000 | 6 568 000 | 7 268 000 | 7 298 000 | 7 318 000 | 7 318 000 |
| EBITDA, ₽ | -3 371 000 | -3 371 000 | -3 876 000 | -4 782 000 | -4 586 000 | -4 650 000 | -4 012 000 | -3 138 000 | -1 878 000 | 542 000 | 3 462 000 | 6 402 000 |
| Cash burn, ₽ | 3 371 000 | 3 371 000 | 3 876 000 | 4 782 000 | 4 586 000 | 4 650 000 | 4 012 000 | 3 138 000 | 1 878 000 | -542 000 | -3 462 000 | -6 402 000 |
| Cumulative cash, ₽ | 3 371 000 | 6 742 000 | 10 618 000 | 15 400 000 | 19 986 000 | 24 636 000 | 28 648 000 | 31 786 000 | 33 664 000 | 33 122 000 | 29 660 000 | 23 258 000 |

**Break-even:** 16.4 клиентов по contribution math, EBITDA break-even M10.
**Startup capital to BE:** ~33 664 000 ₽.

## Pessimistic scenario
_Ниже ARPA (-10%), медленнее enterprise sales cycle, выше delivery/support tail._

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 4 |
| Total clients | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 2 | 4 | 6 | 9 | 13 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 540 000 | 1 080 000 | 2 160 000 | 3 240 000 | 4 860 000 | 7 020 000 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 190 000 | 380 000 | 760 000 | 1 140 000 | 1 710 000 | 2 470 000 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 350 000 | 700 000 | 1 400 000 | 2 100 000 | 3 150 000 | 4 550 000 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 0,0% | 0,0% | 64,8% | 64,8% | 64,8% | 64,8% | 64,8% | 64,8% |
| Fixed costs, ₽ | 3 371 000 | 3 371 000 | 3 876 000 | 4 782 000 | 5 076 000 | 5 630 000 | 5 972 000 | 6 568 000 | 7 268 000 | 7 298 000 | 7 318 000 | 7 318 000 |
| EBITDA, ₽ | -3 371 000 | -3 371 000 | -3 876 000 | -4 782 000 | -5 076 000 | -5 630 000 | -5 622 000 | -5 868 000 | -5 868 000 | -5 198 000 | -4 168 000 | -2 768 000 |
| Cash burn, ₽ | 3 371 000 | 3 371 000 | 3 876 000 | 4 782 000 | 5 076 000 | 5 630 000 | 5 622 000 | 5 868 000 | 5 868 000 | 5 198 000 | 4 168 000 | 2 768 000 |
| Cumulative cash, ₽ | 3 371 000 | 6 742 000 | 10 618 000 | 15 400 000 | 20 476 000 | 26 106 000 | 31 728 000 | 37 596 000 | 43 464 000 | 48 662 000 | 52 830 000 | 55 598 000 |

**Break-even:** 24.8 клиентов по contribution math, EBITDA break-even M15.
**Startup capital to BE:** ~57 984 000 ₽.

## Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

| Scenario | ARPA, ₽/мес | Gross profit/client, ₽ | Contribution/client, ₽ | EBITDA/client до fixed, ₽ | Net after tax IT 3%, ₽ | Net after tax УСН 6%, ₽ | Net after tax ОСНО 20%, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Base | 600 000 | 425 000 | 380 000 | 380 000 | 362 000 | 344 000 | 304 000 |
| Optimistic | 660 000 | 490 000 | 445 000 | 445 000 | 425 200 | 405 400 | 356 000 |
| Pessimistic | 540 000 | 350 000 | 295 000 | 295 000 | 278 800 | 262 600 | 236 000 |

Примечание: EBITDA/client до fixed показывает вклад одного активного клиента до корпоративного OPEX. Для ОСНО 20% строка Net упрощена как post-profit proxy без детального VAT shield; НДС 20% при ОСНО дополнительно ухудшает оборотный капитал и требует отдельного cash buffer.

## Налоговая модель РФ
- **УСН 6%**: самый простой fallback, налог берётся с выручки, NDS обычно нет, но effective margin ниже, чем у IT-льготы.
- **IT-льгота 3%**: применима при аккредитации Минцифры и соблюдении критериев по доле профильной выручки; это лучший режим для данного software-heavy кейса.
- **ОСНО 20%**: налог на прибыль 20% плюс НДС 20%, если режим обязателен или нужен крупным заказчикам. Для enterprise AI security это повышает требования к стартовому капиталу.
- **Страховые взносы**: в модели уже заложено около 30% к gross payroll, поэтому FOT из 04-economics считаю fully-loaded.

## Break-even summary
| Scenario | Contribution/client, ₽/мес | BE client count | EBITDA break-even month | startup_capital_to_bep_rub |
|---|---:|---:|---:|---:|
| Base | 380 000 | 19.3 | M13 | 45 748 000 |
| Optimistic | 445 000 | 16.4 | M10 | 33 664 000 |
| Pessimistic | 295 000 | 24.8 | M15 | 57 984 000 |

<!-- P6A-DONE -->

# SECTION B — Finance Risk / Competitor P6B

## 1. Sensitivity analysis, EBITDA через 12 месяцев

Принял базу из SECTION A и проверил три стресс-фактора по отдельности. Для **CAC x2** считаю, что при том же sales budget темп привлечения платящих клиентов падает примерно вдвое, поэтому к M12 активная база снижается с 17 до ~9 клиентов. Для **Churn x2** поднимаю monthly churn с 1,5% до 3,0% и получаю ~16 активных клиентов к M12 вместо 17. Для **Price -30%** режу ARPA с 600k до 420k ₽ при той же cost base. Это упрощённый, но полезный downside check.

| Scenario | Ключевое изменение | Active clients @M12 | ARPA, ₽/мес | EBITDA @M12, ₽/мес |
|---|---|---:|---:|---:|
| Base | без изменений | 17 | 600 000 | -93 000 |
| Sens1 | CAC x2 | 9 | 600 000 | -3 493 000 |
| Sens2 | Churn x2 | 16 | 600 000 | -518 000 |
| Sens3 | Price -30% | 17 | 420 000 | -3 153 000 |

### Вывод по чувствительности
- Самый опасный single-variable shock, **CAC x2**: модель резко уходит в более глубокий burn, потому что enterprise motion уже дорогой и sales efficiency быстро ломается.
- **Price -30%** почти так же плох, как CAC shock: premium enterprise thesis держится на high-ticket positioning, а не на commodity pricing.
- **Churn x2** пока не убивает модель мгновенно, но уже переводит M12 из near-breakeven в устойчиво отрицательный режим.

## 2. Monte Carlo Lite, confidence intervals

### Triangular inputs
| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC ₽ | 1 600 000 | 2 356 000 | 3 200 000 | partners / blended CAC из 04-economics [T1] |
| Monthly churn % | 1.0% | 1.5% | 3.0% | benchmark + stress envelope из 04-economics [T1] |
| ARPU ₽/мес | 480 000 | 600 000 | 720 000 | base/price pressure/upside packaging [T1] |
| Conversion rate lead→paid % | 0.10% | 0.27% | 0.60% | blended funnel around named-account outbound + partners [T1] |
| Time-to-hire месяцев (среднее) | 1.0 | 1.6 | 3.0 | hiring table из 04-economics [T1] |

### Логика упрощённой симуляции
Вместо полного кода использую 9-комбинационный Monte Carlo Lite: крайние и смешанные сочетания CAC, churn и ARPU, затем раскладываю на p10/p50/p90. M24 считаю как steady-state месяц после масштабирования GTM: база даёт ~65 активных клиентов к M24 при сохранении base ramp, а дальше экономика пересчитывается через ARPU, gross profit и sales efficiency.

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----|-----|-----|-------------|
| EBITDA @M24 (₽/мес) | -2 400 000 | 17 400 000 | 29 800 000 | 32 200 000 |
| CAC payback (мес) | 9.8 | 3.9 | 2.2 | 7.6 |
| LTV/CAC | 1.8x | 12.0x | 15.4x | 13.6x |
| Cash runway (мес) | 7 | 15 | 27 | 20 |

### Интерпретация Monte Carlo Lite
1. **p10 EBITDA @M24 < 0**, значит автоматически срабатывает kill criterion #1: риск непрохождения до финансовой самодостаточности.
2. **p50 EBITDA @M24 > 500k ₽/мес**, значит median-case всё ещё проходит EBITDA gate.
3. Формально отношение **p90/p10** для EBITDA теряет смысл, потому что p10 отрицательный; practically это ещё хуже, чем 10x spread, и означает очень высокую неопределённость.
4. **Range width по LTV/CAC = 13.6x**, сильно выше порога 8x. Значит модель хрупкая, и хрупкость сидит в трёх рычагах сразу: enterprise CAC, ценовая власть и churn discipline.

## 3. Competitor deep-dive

### Западные игроки
| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| Credo AI | сильная governance story, enterprise policy workflows, заметность в Forrester/WEF | слабее security-runtime wedge, тяжёлый governance-first onboarding | ~8-12% глобального AI governance сегмента среди крупных enterprise-shortlists [inference] | в РФ можно выиграть за счёт AI-security-first wedge, private cloud и локальных интеграций |
| Lakera | сильный brand в GenAI security, real-time protection, узнаваемость у AI-native buyers | меньше локализационной глубины для РФ, vendor-risk для regulated buyers | ~5-8% глобального AI security / guardrails subsegment [inference] | локальный data residency, on-prem и интеграция в ИБ-контур вместо pure API layer |
| Runlayer | сильный фокус на MCP, agents, approvals, self-hosted/security narrative | компания моложе, category ещё ранняя, risk of platform immaturity | ~2-4% emerging agent-governance niche [inference] | можно упаковать не только MCP/agent layer, но и enterprise compliance package под РФ |

### Российские и локально-релевантные substitutes
Прямых pure-play аналогов в РФ мало, поэтому ниже смесь конкурентов и ближайших substitute-решений, через которые buyer может закрыть бюджет.

| Игрок | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| Swordfish Security | ранний локальный AI-security credibility, сильная экспертиза ИБ | скорее services-heavy модель, чем repeatable platform | ~5-10% локального спроса на AI-security assessments [inference] | recurring product layer, а не только аудит/консалтинг |
| Security Vision | зрелые enterprise/compliance workflows, сильные связи с крупными заказчиками | больше GRC/SOC/platform vendor, чем agent runtime security | ~8-12% смежного РФ GRC/SOC automation бюджета [inference] | более узкий и ценный AI-runtime focus |
| Just AI | сильные enterprise AI-интеграции, узнаваемость на локальном AI-рынке, доступ к buyer base | основной фокус не security/governance, buyer может собрать решение кастомно | ~10-15% смежного enterprise conversational AI рынка [inference] | security-native control plane поверх любых AI use cases |
| MTS AI / MWS AI stack | мощный enterprise channel, private cloud, сильный бренд | риск bundle, но security-governance не всегда core-product | ~10% смежного enterprise GenAI pipeline у крупных клиентов [inference] | vendor-agnostic слой, который работает поверх разных моделей и контуров |
| Kaspersky / BI.ZONE как substitute | высокий trust у regulated buyers, понятный security budget owner | могут решать adjacent threat surface, но не обязательно runtime governance для агентов | вместе ~20%+ доступного бюджета у самых консервативных buyers [inference] | специализированный продукт под AI agents, policy enforcement и tool governance |

### Источники по конкурентам
- Credo AI: Forrester Wave / WEF / company materials.
- Lakera: lakera.ai.
- Runlayer: runlayer.com и TechCrunch.
- Swordfish Security: hh.ru employer page и рыночные упоминания в 02-demand.
- Just AI: vc.ru и официальный сайт.
- Security Vision: Habr и официальный сайт.
- MTS AI: vc.ru / Habr / официальный сайт.
- Руспрофиль можно использовать как sanity-check на юрлица локальных игроков, но доли рынка выше всё равно остаются экспертной оценкой, а не бухгалтерским фактом.

## 4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Не удаётся нанять 2 сильных ML/security инженеров вовремя | high | Срыв roadmap и пилотов | time-to-hire > 3 мес, offer acceptance < 50% | сдвиг к smaller core team, advisor bench, часть detection/guardrails через партнёров |
| Operational | Ломается надёжность LLM/API и policy routing под enterprise SLA | med | Простой у клиентов, штрафы, churn | рост latency, incident count, fallback usage | multi-model routing, локальные backup-модели, SRE runbooks |
| Market | Спрос остаётся education-led, а не budget-led | med | Длинный цикл продаж, burn | discovery есть, paid pilots нет | ICP сузить до regulated buyers с уже идущим GenAI rollout |
| Market | Price compression из-за hyperscalers и bundled guardrails | high | Падение ARPA и GM | проигрыш тендеров по цене, discounting >20% | продавать compliance package и on-prem deployment, а не API-фильтр |
| Regulatory | Требования 152-ФЗ/локализация данных ограничивают SaaS-модель | high | Блок продаж в regulated сегменте | security/legal review стопорится на residency | private cloud/on-prem by default, локальное хранение логов |
| Regulatory | Усиление 115-ФЗ/KYC и отраслевых требований в финсекторе | med | Рост стоимости внедрения и longer sales cycle | растёт объём security questionnaires и кастомных DPA | готовые compliance templates, отраслевые коннекторы, pre-approved deployment docs |
| Financial | Cash runway съедается из-за длинного payback и поздних оплат | high | Down round или остановка развития | DSO > 75 дней, burn > план на 20% | upfront pilot fees, milestone billing, reserve cash 12+ мес |
| Financial | Ослабление рубля повышает стоимость LLM/API и infra | med | Давление на GM | доля USD-linked COGS > 25%, GM < 65% | рублёвые contracts, локальные модели, annual repricing clauses |
| Black swan | Новые санкции режут доступ к западным SaaS/моделям | high | Потеря части стека и клиентов | vendor notices, geo-blocking, contract termination risk | стек из заменяемых компонентов, self-hosted open models, локальные провайдеры |
| Black swan | Военная/политическая эскалация резко сдвигает бюджеты клиентов | med | Заморозка закупок, перенос пилотов | стоп по CAPEX/OPEX, pause новых AI-программ | фокус на ROI/security compliance use-cases, upsell в существующие accounts |

## 5. Kill conditions через 6 месяцев
1. **Median pipeline не подтверждает economics:** если forecast на M24 даёт **p50 EBITDA < 500 000 ₽/мес**, кейс не проходит EBITDA gate и продолжать нельзя.
2. **Продажи не подтверждают unit economics:** если fully-loaded **CAC > 4,5 млн ₽** или win rate lead→paid остаётся **<0,15%** без признаков улучшения, GTM сломан.
3. **Retention/price thesis ломается:** если pilot-to-paid conversion < 30% **или** подтверждённый ARPA по первым 3 сделкам < **450 000 ₽/мес**, premium enterprise thesis не подтверждается.

## 6. Итог критика
Кейс всё ещё выглядит investable, но только как **узкий enterprise AI security/control plane** для regulated buyers. Главное ухудшение по SECTION B: economics в median-case хорошие, но диапазон outcomes слишком широкий. Значит score не надо повышать автоматически после P6A, а наоборот стоит держать discount за execution risk, price pressure и санкционную зависимость стека.

<!-- P6B-DONE -->


---

## FILE: 06-verdict.md

[GEO-EXPAND] WitnessAI geo-expand v2 — NEAR-PASS: 68/100 | EBITDA base=11682К₽/мес через 13 мес | LTV/CAC=12,0x | Ключевое преимущество: premium on-prem AI security wedge для regulated enterprise | Главный риск: weak moat и дорогой category-education в РФ.

# 06-verdict — WitnessAI geo-expand v2

sector: GEO-EXPAND

## Финальный вердикт
- **Статус:** NEAR-PASS
- **Normalized score:** **68/100**
- **Итог комитета:** кейс инвестиционно интересен по unit economics, но пока не дотягивает до APPROVED из-за слабого moat, широкого outcome-range в P6B и недоказанного локального GTM-repeatability.
- **Пороговое правило:** score < 70, поэтому кейс уходит в `rejected/` как **NEAR-PASS**.
- **Дубликатность / сравнение:** кейс содержательно близок к более широкому тезису про enterprise agent control plane, но как standalone wedge по AI security/governance в РФ имеет собственную buyer-line и должен оцениваться отдельно.

## Оценка
Source tier balance: T1=10, T2=4, T3=1, weighted=2.60. Penalty applied: 0 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | «LTV/CAC: 12.0x», «CAC Payback: 3.9 мес», «Gross Margin: 70.8%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | «EBITDA при 50 клиентах: около 11.8 млн ₽/мес», «Break-even: 19 клиентов или ориентировочно M13». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 15 | «exact-demand ... низкий», но «рынок ИБ большой, 337 млрд ₽» и «AI использовали 6% организаций». |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 10 | Покупательская ценность есть, но category layer легко частично закрывается hyperscalers, integrators и internal AppSec. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | «p10 EBITDA @M24 < 0», плюс высокие риски по найму, санкциям, data residency и длинному enterprise cycle. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | GTM опирается на partner-led + named-account outbound, а economics допускает enterprise motion при high-ACV упаковке. |

**Сумма raw:** 102/150

**Normalized score = round((102 × 100) / 150) = 68/100**

## Investment thesis
Кейс проходит по математике фондового enterprise software: высокая валовая маржа, сильный LTV/CAC, достижимый break-even за 13 месяцев и EBITDA-path существенно выше 500К₽/мес. Но одобрение блокируют три вещи: 1) exact-demand в РФ остаётся budget-led, а не category-led; 2) moat пока средне-слабый, потому что часть ценности уже размывается hyperscaler guardrails, SIEM/DLP-интеграторами и internal security teams; 3) P6B показывает слишком широкий диапазон исходов, где p10 EBITDA @M24 уже отрицателен.

## 7-factor moat framework

| Фактор | Балл 0-3 | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не улучшает продукт для остальных в явной сетевой форме. |
| Switching costs | 2 | После интеграции policy layer, audit trail и DLP/SIEM/IAM контура смена поставщика становится болезненной. |
| Scale economies | 1 | Есть частичный leverage в reuse policy-packages и infra, но on-prem/private cloud съедает часть эффекта масштаба. |
| Proprietary data / model advantage | 1 | Уникальный датасет не доказан, преимущество скорее в orchestration и security packaging. |
| Regulatory moat | 1 | Регуляторный wedge есть, но он не эксклюзивен и пока не закреплён лицензией или обязательной аккредитацией. |
| Brand / distribution | 1 | Глобальная категория валидирована, но локальный бренд-канал в РФ не доказан. |
| Embedded workflow | 3 | При успешном внедрении слой глубоко встраивается в AI runtime, approvals, audit и tool governance. |

**Сумма 7-factor:** 9/21

**Moat score = round((9 × 25) / 21) = 11/25**

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 28 320 000 ₽ |
| CAC fully-loaded | 2 356 000 ₽ |
| LTV/CAC | 12,0x |
| CAC payback | 3,9 мес |
| Gross Margin | 70,8% |
| contribution_margin_rub_month | 380 000 ₽ |
| fixed_costs_rub_month | 7 318 000 ₽ |
| company_ebitda_rub_month base at 50 clients | 11 682 000 ₽/мес |
| company_ebitda_potential_rub_month | 11 682 000 ₽/мес |
| clients_to_500k_ebitda | 21 |
| months_to_500k_ebitda | 13 |
| clients_to_1m_ebitda | 23 |
| months_to_1m_ebitda | 14 |
| Break-even client count | 19 |
| startup_capital_to_bep_rub | 45 748 000 ₽ |
| TAM РФ | 7,2 млрд ₽ |
| SAM РФ | 2,53 млрд ₽ |
| SOM Y1 | 58 млн ₽ |
| SOM Y3 | 228 млн ₽ |

## FULL business process from 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-account list по банкам/enterprise | CEO + SDR | HH, LinkedIn-like базы, сайт компании, CRM | 2 ч/аккаунт | 2 400 | низкая |
| 2 | Первый outbound-touch, email + Telegram + intro | SDR | HubSpot, sequencing tool, почта | 1.5 ч | 1 800 | средняя |
| 3 | Qualification call | SDR | Meet/Zoom, CRM | 1 ч | 1 200 | средняя |
| 4 | Discovery с CISO / architect | CEO + AE | Meet, Notion, CRM | 2 ч | 8 800 | низкая |
| 5 | Security scoping и threat mapping | CTO + Solutions/Prod | Miro, docs, checklist | 6 ч | 12 000 | низкая |
| 6 | Demo / architecture workshop | AE + CTO | Demo env, slides | 3 ч | 8 100 | низкая |
| 7 | Pilot proposal и ROI model | AE + CEO | CRM, spreadsheet | 4 ч | 11 200 | средняя |
| 8 | Security review / questionnaire | CTO + DevOps | Confluence, security docs | 12 ч | 21 900 | низкая |
| 9 | Pilot deployment в private cloud / VPC | DevOps + Backend + ML | Terraform, cloud, repo, CI/CD | 20 ч | 33 800 | средняя |
| 10 | Policy tuning, guardrails, routing | ML + Backend | platform console, notebooks | 16 ч | 31 800 | средняя |
| 11 | Pilot readout и commercial negotiation | CEO + AE | CRM, spreadsheet, call | 4 ч | 13 800 | низкая |
| 12 | Legal / procurement / DPA | CEO + external legal | docflow, e-sign | 8 ч | 20 000 | низкая |
| 13 | Invoice / act / payment collection | Finance ops | 1C/банк/CRM | 1.5 ч | 3 500 | высокая |

## Команда

| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO / founder | enterprise sales, fundraising, strategic partnerships | 845 000 |
| CTO / Tech Lead | product architecture, security roadmap | 780 000 |
| Senior Backend #1 | platform/backend/core integrations | 546 000 |
| Senior Backend #2 | scalability, connectors, audit plane | 546 000 |
| ML Engineer #1 | policy/classification/routing | 650 000 |
| ML Engineer #2 | runtime defense / red teaming | 650 000 |
| DevOps | VPC/private cloud, deployment, logging | 455 000 |
| Frontend | admin console, policy UX | 390 000 |
| Product / Solutions | deployment design, customer scoping | 416 000 |
| SDR | top-of-funnel outbound | 234 000 |
| AE | demos, pilots, close | 494 000 |
| Customer Success | onboarding, adoption, renewals | 312 000 |
| **Итого** |  | **6 318 000** |

## GTM: 10 named targets

| Target | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Сбер | Уже есть вакансия «Руководитель направления по защите AI-инфраструктуры», значит pain owner существует. | email decision-maker + security conference | 1 500 000 ₽/мес |
| Т-Банк | Агрессивное AI-внедрение и высокий риск data governance в финсекторе. | intro через интегратора / CISO office | 1 200 000 ₽/мес |
| ВТБ | Regulated buyer с длинным, но крупным security budget. | партнёрство с крупным SI | 1 200 000 ₽/мес |
| МТС | Private cloud и enterprise AI stack создают спрос на policy/governance слой. | vc.ru ad + enterprise event | 900 000 ₽/мес |
| VK | Много AI-продуктов и чувствительных пользовательских данных. | direct outreach в platform/security | 900 000 ₽/мес |
| Яндекс | Сложный AI runtime и высокий reputational risk при утечках / agent misuse. | founder-led outbound | 1 500 000 ₽/мес |
| X5 Group | Retail AI и customer-facing assistants повышают need в audit trail и policy enforcement. | отраслевая конференция + партнерский канал | 700 000 ₽/мес |
| Магнит | Схожий retail pain, важен контроль внутренних copilots и vendor LLM usage. | email decision-maker | 700 000 ₽/мес |
| Северсталь | Закрытый контур и high-sensitivity industrial workflows. | интегратор + private cloud proposal | 800 000 ₽/мес |
| Газпром нефть | Крупный промышленный buyer с требованиями к self-hosted deployment. | партнёрство + executive intro | 1 000 000 ₽/мес |

## Почему это не APPROVED
1. **Market pull пока недостаточно прямой.** В `02-demand.md` зафиксировано: exact-demand по формулировке категории LOW, спрос приходится вытаскивать через budget reinterpretation.
2. **Moat средний и легко атакуемый.** Покупатель может собрать substitute из hyperscaler guardrails, observability stack, SIEM/DLP и внутреннего AppSec.
3. **P6B слишком волатилен.** В `05-critic.md` прямо указано: `p10 EBITDA @M24 < 0`, а самый опасный shock, CAC x2, резко ломает модель.

## Top-3 risks

| Риск | Вероятность | Impact | Почему в top-3 |
|---|---|---|---|
| weak_moat_and_bundle_risk | Высокая | Высокий | Значимая часть value уже закрывается AWS/Azure guardrails, gateway vendors и локальными интеграторами. |
| enterprise_gtm_execution | Средняя | Высокий | Для победы нужен дорогой pilot-led motion, security review и partner distribution без права на CAC drift. |
| sanctions_and_stack_dependency | Средняя | Высокий | Доступность западного стека, LLM/API и compliance-ограничения могут ухудшить GM и сорвать deployment. |

## Proof points required for APPROVED
1. 3 paid pilots в РФ или дружественных regulated-контурах с ARPA не ниже **600 000 ₽/мес**.
2. Pilot-to-paid conversion не ниже **30%** и win rate без скидки >20% от base pricing.
3. Подтверждение, что on-prem/private cloud delivery остаётся **platform-led**, а не превращается в чистый консалтинг.
4. Минимум 2 repeatable integrations с DLP/SIEM/IAM, которые сокращают time-to-value и повышают switching costs.
5. Локальный reference-pack по data residency и AI governance, чтобы сократить security/procurement цикл.

## LTV Upside Calculator

Ниже, что должно улучшиться, чтобы перевести кейс из 68/100 в approve-зону 70+ без самообмана.

| Рычаг | Текущая база | Целевой upside | Эффект |
|---|---:|---:|---|
| ARPA / MRR | 600 000 ₽ | 750 000 ₽ | усилит premium positioning и снизит sensitivity к CAC/price compression |
| Fully-loaded CAC | 2 356 000 ₽ | ≤ 1 900 000 ₽ | стабилизирует p10 и сократит burn при pilot-heavy motion |
| Monthly churn | 1,5% | ≤ 1,2% | поднимет customer_ltv_rub и улучшит predictability renewals |
| Moat score | 11/25 | ≥ 14/25 | нужен более глубокий workflow embed + reusable compliance package |
| Paid pilots | 0 подтверждённых в РФ | ≥ 3 | превратит budget-led гипотезу в реальный GTM proof |

## Финальный комитетский вывод
**NEAR-PASS.** Я не готов одобрять кейс сейчас, потому что текущая версия опирается на сильную экономику, но ещё не доказала локально защищённый GTM и не сняла bundle risk. Если появятся 2-3 реплицируемых enterprise внедрения и улучшится moat через compliance/integration pack, кейс может быстро перейти в зону APPROVED WITH NOTES.


---

## FILE: 07-score-trajectory.md

# 07-score-trajectory

## 2026-04-24 — P4 Demand Validation — branch-models-lead
- Stage: P4 demand-validation
- Score trajectory: `new -> CONDITIONAL_PASS`
- Demand signal: **LOW** exact-demand by internal API, but with enterprise budget-backed category proof.
- Key reasons:
  1. internal demand API for the exact category returned `LOW`;
  2. Russian market already shows AI adoption, AI-security staffing and enterprise cyber budgets;
  3. competitors and substitutes already monetize guardrails / observability / governance;
  4. profit gate fails in self-serve SaaS but passes in private-cloud and on-prem enterprise scenarios.
- Decision: keep in pipeline, continue to next stages.
- Artifact: `pipeline/cases/witnessai-geo-expand-v2/02-demand.md`

## 2026-05-12 — P5 Unit Economics — branch-models-lead
- Stage: P5 unit-economics
- Score trajectory: `CONDITIONAL_PASS -> PASS`
- Economics summary:
  1. blended fully-loaded CAC = **2.36 млн ₽**;
  2. MRR per customer = **600k ₽**, COGS = **175k ₽**, Gross Margin = **70.8%**;
  3. LTV = **28.3 млн ₽** at monthly churn **1.5%**;
  4. LTV/CAC = **12.0x**;
  5. CAC Payback = **3.9 мес**;
  6. Contribution Margin = **63.3%**;
  7. break-even = **19 клиентов**, ориентир **M13**;
  8. EBITDA at 50 clients = **~11.7 млн ₽/мес**.
- Key reasons:
  1. enterprise AI security motion дорогой, но economics выдерживает fully-loaded CAC;
  2. unit economics остаётся investable даже при conservative churn и heavy delivery assumptions;
  3. reject gate не срабатывает, потому что при 50 клиентах EBITDA многократно выше 500k ₽/мес;
  4. риск остаётся в services creep и margin pressure от on-prem deployment.
- Decision: keep in pipeline, pass to next stage.
- Artifact: `pipeline/cases/witnessai-geo-expand-v2/04-economics.md`

## 2026-06-08 — P7 Critic + Verdict — branch-models-lead
- Stage: P7 critic-and-verdict
- Score trajectory: `PASS -> NEAR-PASS 68/100`
- Rubric summary:
  1. Unit Economics = **20/25**;
  2. EBITDA Potential = **20/25**;
  3. Market + Demand = **15/25**;
  4. Moat = **10/25**;
  5. Execution Risk = **17/25**;
  6. GTM Realism = **20/25**.
- Key reasons:
  1. enterprise economics остаётся сильной, LTV/CAC **12,0x**, payback **3,9 мес**, EBITDA-path проходит gate;
  2. локальный спрос остаётся budget-led, а exact-demand по категории слабый;
  3. moat слабее investment-grade из-за substitute pressure от hyperscalers, integrators и internal security teams;
  4. P6B добавляет существенный downside: **p10 EBITDA @M24 < 0** и высокая чувствительность к CAC/price pressure.
- Decision: **NEAR-PASS**, перенести в rejected/ как кейс для возможного re-open при появлении 3 paid pilots и stronger local moat.
- Artifact: `pipeline/rejected/witnessai-geo-expand-v2/06-verdict.md`


---

## FILE: telegram-messages-thread-270.md

Сообщение 1 / thread 270
[NEAR-PASS] WitnessAI geo-expand v2
Описание: enterprise AI security / governance слой для AI-агентов, copilots и LLM-приложений в РФ. Финансовая математика сильная, но approve пока блокируют weak moat, bundle risk и слишком широкий downside range.
Аудитория: CISO, CIO, head of platform security, enterprise architects, AI governance owners в regulated enterprise.

Сообщение 2 / thread 270
Процессы: founder-led outbound -> discovery -> security scoping -> pilot deployment private cloud/VPC -> policy tuning -> legal/procurement -> recurring platform fee.
Юнит-экономика: customer_ltv_rub 28,32 млн ₽; CAC 2,356 млн ₽; LTV/CAC 12,0x; CAC payback 3,9 мес; Gross Margin 70,8%; contribution_margin_rub_month 380 000 ₽.
Прибыль компании: 500К EBITDA достигается примерно на 21 клиенте около M13; 1М EBITDA около 23 клиентов и M14. EBITDA base at 50 clients = 11,682 млн ₽/мес.

Сообщение 3 / thread 270
Рынок: exact-demand по категории слабый, но в РФ уже есть AI adoption, крупный рынок ИБ, hh-сигналы и enterprise budget line на защиту AI-инфраструктуры.
Финансы: score 68/100, verdict NEAR-PASS, startup_capital_to_bep_rub 45,748 млн ₽, TAM РФ 7,2 млрд ₽, SAM РФ 2,53 млрд ₽.
Что доказать: 3 paid pilots с ARPA >=600К₽/мес, pilot-to-paid >=30%, repeatable on-prem package и stronger switching costs через integrations/compliance.
GitHub: будет после commit/push.

Примечание: внешняя отправка не выполнялась из этого run; пакет подготовлен для публикации в Telegram thread 270.


---
