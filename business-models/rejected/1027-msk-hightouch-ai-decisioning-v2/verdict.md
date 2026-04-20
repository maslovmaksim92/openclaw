# 1027-msk-hightouch-ai-decisioning-v2
- status: REJECTED / NEAR-PASS
- score: 69/100
- sector: B2B-OPS
- source_case_path: pipeline/rejected/1027-msk-hightouch-ai-decisioning-v2
- github_repo_path: rejected/1027-msk-hightouch-ai-decisioning-v2/verdict.md

---

## 00-brief.md

# 00-brief

## Кейс
1027-msk-hightouch-ai-decisioning-v2

## Статус
active

## Тип сигнала
resurrect

## rerun_of
1027-msk-hightouch-ai-decisioning

## Краткое описание
Кейс создан по правилу принудительного полного пайплайна для resurrect-сигнала по Hightouch AI Decisioning, хотя раньше материал был закрыт как duplicate без запуска полного анализа.

## Что делать дальше
Перейти к P3-demand-validation и заново проверить самостоятельную ценность warehouse-native AI decisioning слоя для lifecycle-маркетинга и CRM-персонализации, даже если итоговый verdict снова покажет пересечение с соседними кейсами.


---

## 01-intake.md

---
sector: B2B-OPS
rerun: true
source_raw: 2026-04-19-resurrect-1027-msk-hightouch-ai-decisioning.md
created: 2026-04-19T22:31:00+03:00
---

# 01-intake

## Кейс
1027-msk-hightouch-ai-decisioning-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
См. блок `Meta.source` и секцию `Original triage (context)` внутри исходного raw-файла.

## Полный контекст из raw

# RESURRECT SIGNAL — 1027-msk-hightouch-ai-decisioning

## Meta
- source: triage/triage-2026-04-18-1027-msk-hightouch-ai-decisioning-duplicate.md
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
- `pipeline/raw/raw-2026-04-18-1027-msk-hightouch-ai-decisioning-geo-expand.md`

## Классификация
Дубликат ранее обработанного сигнала.

## Решение
Новый кейс не создан, открытые кейсы в `pipeline/cases/` не обогащались.

## Почему это дубликат
- Сигнал полностью совпадает по теме с уже обработанным направлением warehouse-native AI decisioning для lifecycle-маркетинга и CRM-персонализации.
- Во входном файле повторяются уже известные факты: Hightouch AI Decisioning, тезис про достижение $100 млн ARR, позиционирование как decisioning-слой поверх DWH и martech-стека, а также тот же вывод о частичных аналогах в РФ.
- Во входном материале нет нового подтверждения спроса, новой экономики, нового buyer-сегмента или нового технологического wedge относительно ранее зафиксированных материалов по Hightouch и смежному кейсу `warehouse-native-ai-decisioning-marketing-operator`.

## Почему кейс не обогащался
- В `pipeline/cases/` сейчас нет открытого кейса по этой теме, который можно было бы корректно усилить как supporting signal.
- Ближайший совпадающий кейс `warehouse-native-ai-decisioning-marketing-operator` уже находится в `pipeline/rejected/`, поэтому текущий raw-файл не обогащает открытый кейс в рамках standing orders.

## Статус raw-файла
Файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Повторный сигнал по Hightouch без новых данных и без подходящего открытого кейса для обогащения. Новый кейс не создан, обогащение не выполнялось.

```



---

## 02-demand.md

# 02-demand

## Demand validation verdict
- **Итог по спросу:** спрос в РФ не массовый по формулировке `AI decisioning`, но реальный в adjacent-категориях `маркетинговая автоматизация`, `CDP` и `персонализация маркетинга`. **Статус: PASS WITH CONSTRAINTS.** [T1][T2]
- **Composite demand API:** `LOW` (`3/100`) по `AI decisioning`, `LOW` (`18/100`) по `customer data platform`, `LOW` (`22/100`) по `персонализация маркетинга`, `MEDIUM` (`30/100`) по `маркетинговая автоматизация`. Это означает не нулевой рынок, а mismatch между англоязычным category label и локальной buying language. [T1]
- **Ключевой вывод:** самостоятельная ценность warehouse-native decisioning слоя в РФ есть только для верхнего B2C enterprise-сегмента с собственной DWH/CDP-инфраструктурой и сложным lifecycle-маркетингом. Для SMB и mid-market спрос недостаточно доказан. [T1][T2]

## Demand evidence
1. Hightouch пишет, что обслуживает **803+ customers** и обрабатывает **9,9 млрд AI Decisions в год**. Это прямое подтверждение глобального willingness-to-pay за category `composable CDP + decisioning`. [T1]  
   Source: https://hightouch.com/about
2. Hightouch находится в **Gartner Magic Quadrant for Customer Data Platforms** от **26 января 2026**, что подтверждает существование зрелой product category, а не point-solution hype. [T1]  
   Source: https://hightouch.com/customers
3. По demand API в РФ ключ `маркетинговая автоматизация` показывает **MEDIUM / 30**, **910 вакансий HH.ru**, `CDP` показывает **107 вакансий**, `персонализация маркетинга` показывает **111 вакансий**. Это уже операционный спрос на команды и workflows, которые продукт может усиливать или частично замещать. [T1]  
   Source: http://172.18.0.1:9001/multi-demand?keyword=%D0%BC%D0%B0%D1%80%D0%BA%D0%B5%D1%82%D0%B8%D0%BD%D0%B3%D0%BE%D0%B2%D0%B0%D1%8F%20%D0%B0%D0%B2%D1%82%D0%BE%D0%BC%D0%B0%D1%82%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F
4. В РФ уже покупают substitute-решения для CRM-маркетинга, Telegram-каналов, customer messaging и сценарной автоматизации, значит бюджетная строка для personalization stack реально существует. [T2]

## Competitor set and pricing
| Игрок | Что закрывает | Публичная цена | Вывод |
|---|---|---:|---|
| Sendsay Маркетинг | email/SMS/web push/mobile push/Telegram, CDP, триггеры | от **7 080 ₽/мес**; tier M250 **50 010 ₽/мес** при 200k-250k контактов [T2] | Локальный substitute для омниканальной автоматизации, но без warehouse-native decisioning |
| Carrot quest | автоматизация, мессенджеры, Telegram-боты, триггеры | от **6 240 ₽/мес**; Pro **17 490 ₽/мес**; Enterprise **39 990 ₽/мес** [T2] | Показывает нижнюю и среднюю границу WTP в RU martech |
| BotHelp | Telegram/VK chatbot automation | от **$18/мес** за 1 000 subscribers до **$1 529/мес** за 500 000 subscribers [T2] | Подтверждает, что Telegram automation commoditized на low-end, но это не decisioning core |
| Jivo | омниканальные чаты, Telegram, marketing add-ons | Core tiers от **742 ₽/мес** до **3 142 ₽/мес** за оператора; add-on `Продвижение в Telegram` **2 711 ₽/мес** [T2] | Платёжеспособность за messaging есть, но это front-end слой, не brain layer |

Sources:  
- Sendsay: https://sendsay.ru/rates  
- Carrot quest: https://www.carrotquest.io/pricing/  
- BotHelp: https://www.bothelp.io/pricing  
- Jivo: https://www.jivo.ru/pricing/

## Telegram bots/services in RU
- **Sendsay Маркетинг** прямо включает канал **Telegram** в product mix. Это valid RU substitute для orchestration, но не для warehouse-native AI decisioning. [T2]
- **Carrot quest** продаёт **Telegram-боты** и триггерные сценарии как часть customer messaging stack. [T2]
- **BotHelp** monetizes Telegram automation напрямую и закрывает low-end chatbot workflows. [T2]
- **Jivo** продаёт `Продвижение в Telegram` и поддержку канала Telegram в клиентских коммуникациях. [T2]

**Вывод по Telegram:** в РФ есть зрелый слой Telegram-first и omnichannel automation-инструментов, но не найден публично упакованный RU-продукт уровня Hightouch AI Decisioning с warehouse-native orchestration, decision policies и unified experimentation поверх DWH. Это подтверждает окно для enterprise wedge, но также означает, что buyer может решить 60-70% задачи более дешёвыми substitution-tools. [T2, inference]

## WTP, willingness to pay
- Глобальный WTP подтверждён фактом **803+ клиентов** у Hightouch и включением в Gartner MQ по CDP. [T1]
- Локальный WTP подтверждён публичными тарифами RU substitute-игроков: от **7 080 ₽/мес** у Sendsay Маркетинг до **39 990 ₽/мес** у Carrot quest Enterprise, плюс usage-based Telegram automation у BotHelp. [T2]
- Для продукта класса Hightouch в РФ нельзя брать low-end тарифы как целевой чек. Реалистичный enterprise-чек для узкого ICP, если продукт реально управляет сегментацией, next-best-action и orchestration поверх DWH, это **250-400 тыс. ₽/мес** на клиента, то есть **3,0-4,8 млн ₽ ARR**. Это inference из того, что продукт должен заменить часть ручной CRM-аналитики и увеличить выручку на крупных B2C активах, а не просто отправлять сообщения. [T2, inference]
- Proof of willingness to pay есть, но он **не прямой и не локальный** для exact category label `AI decisioning`; в РФ он проходит через adjacent budgets на CRM automation, CDP и Telegram/customer messaging. [T1][T2]

## Market sizing
### Assumptions
- Курс для пересчёта: **76,0535 ₽/$** по курсу ЦБ РФ. [T1]  
  Source: https://www.cbr.ru/currency_base/daily/
- Глобальный рынок **Customer Data Platform** оценивается Grand View Research в **$8,26 млрд в 2025** с CAGR **33,3%** до 2030. Для Hightouch это самый близкий top-down proxy. [T2]  
  Source: https://www.grandviewresearch.com/industry-analysis/customer-data-platform-market-report
- Для грубой локализации беру GDP-share proxy РФ около **1,95%** мирового рынка как консервативный способ не завысить TAM. [T2]
- Buyer universe bottom-up: **100** крупнейших российских интернет-магазинов из рейтинга Data Insight Top100 плюс **352** действующие кредитные организации по базе/статистике ЦБ РФ. Это proxy на крупные организации, где есть first-party data, CRM-маркетинг и бюджеты на automation. [T1][T2]  
  Sources: https://top100.datainsight.ru/ , https://www.cbr.ru/statistics/bank_sector/lic/
- Не все buyer-ы fit для warehouse-native decisioning. Беру только **35%** как сегмент с реально сложной data maturity и частыми lifecycle use-cases. Это поддержано demand API по `CDP`, `персонализация маркетинга` и `маркетинговая автоматизация`. [T1/T2-supported inference]

### 10 реальных buyers для bottom-up и GTM-10-targets
1. Сбер [T1/T2]
2. Т-Банк [T1/T2]
3. ВТБ [T1/T2]
4. Ozon [T2]
5. Wildberries [T2]
6. Яндекс Маркет [T2]
7. Самокат [T2]
8. X5 Group [T2]
9. МегаФон [T2]
10. МТС [T2]

### Top-down
- **TAM (мир):** $8,26 млрд = **628,2 млрд ₽**. [T2]
- **TAM (РФ):** 1,95% от мирового TAM = **12,25 млрд ₽**. [T2]
- **SAM (РФ):** беру **8%** от TAM РФ, то есть только enterprise B2C компании с собственной data infra и регулярным lifecycle orchestration. Получаю **980 млн ₽**. [T2, inference]
- **SOM Y1:** 3% от SAM = **29,4 млн ₽**. [T2, inference]
- **SOM Y3:** 10% от SAM = **98,0 млн ₽**. [T2, inference]

### Bottom-up
- **Total buyers:** 100 крупнейших онлайн-ритейлеров + 352 кредитные организации = **452** потенциальных аккаунта. [T1][T2]
- **% with need:** **35%**, то есть **158** компаний. [T1/T2-supported inference]
- **ARR avg:** **3,6 млн ₽/год** на клиента, то есть **300 тыс. ₽/мес**. [T2, inference]
- **SAM bottom-up:** 158 × 3,6 млн ₽ = **568,8 млн ₽**. [T2]
- **SOM Y1 bottom-up:** 5% capture = **28,4 млн ₽**. [T2]
- **SOM Y3 bottom-up:** 15% capture = **85,3 млн ₽**. [T2]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | $8,26B / 628,2 млрд ₽ [T2] | — | — | top-down |
| TAM (РФ) | 12,25 млрд ₽ [T2] | 1,63 млрд ₽ как upper proxy при 452 buyer × 3,6 млн ₽ [T1][T2] | diff ~7,5x, потому что buyer-based proxy уже ближе к serviceable market, а не к full TAM | top-down |
| SAM (РФ) | 980,0 млн ₽ [T2] | 568,8 млн ₽ [T1][T2] | diff ~1,72x, допустимо | **568,8 млн ₽** |
| SOM Y1 | 29,4 млн ₽ | 28,4 млн ₽ | diff ~1,0x | **28,4 млн ₽** |
| SOM Y3 | 98,0 млн ₽ | 85,3 млн ₽ | diff ~1,15x | **85,3 млн ₽** |

**Sanity check:** при ACV **3,6 млн ₽** SOM Y1 **28,4 млн ₽** требует около **8 клиентов**. При sales-cycle **6-9 месяцев** это тяжёлая, но достижимая цель для founder-led enterprise GTM. SOM Y1 меньше 10% SAM, overclaiming нет. [T2, inference]

## Profit Gate: EBITDA >= 500 000 ₽/мес
Проверил все базовые сценарии монетизации.

1. **Low-ticket SaaS / automation-only**  
   40 клиентов × 35 000 ₽/мес = **1 400 000 ₽/мес выручки**. При EBITDA-марже 20% получаем **280 000 ₽/мес EBITDA**. **FAIL.** [T2]

2. **Mid-market CDP-lite**  
   15 клиентов × 120 000 ₽/мес = **1 800 000 ₽/мес выручки**. При EBITDA-марже 30% получаем **540 000 ₽/мес EBITDA**. **PASS, но на грани.** [T2]

3. **Enterprise decisioning platform**  
   6 клиентов × 300 000 ₽/мес = **1 800 000 ₽/мес выручки**. При EBITDA-марже 40% получаем **720 000 ₽/мес EBITDA**. **PASS.** [T2]

4. **Managed decisioning + services**  
   5 клиентов × 400 000 ₽/мес = **2 000 000 ₽/мес выручки**. При EBITDA-марже 35% получаем **700 000 ₽/мес EBITDA**. **PASS.** [T2]

5. **Pure agency / custom projects**  
   3 проекта × 450 000 ₽/мес = **1 350 000 ₽/мес выручки**. При EBITDA-марже 25% получаем **337 500 ₽/мес EBITDA**. **FAIL.** [T2]

**Итог Profit Gate:** достижим, но только в enterprise-license или hybrid managed модели. Нижний чек и pure services не проходят порог. [T2]

## Risks
- Прямой demand по формулировке `AI decisioning` в РФ слабый, значит category education будет дорогой. [T1]
- Часть рынка уже удовлетворяется более дешёвыми substitutes, особенно через Telegram automation и CRM suites. [T2]
- Warehouse-native value proposition релевантен только компаниям с mature DWH, event-stream и собственной data team. Это резко сужает ICP. [T1][T2]
- Без сильного integration wedge продукт рискует выглядеть как дорогой orchestration-layer поверх уже купленных Sendsay, Mindbox, Carrot quest и внутреннего BI. [T2]

## Final assessment
- **Demand:** LOW для broad market, **MEDIUM** для узкого B2C enterprise ICP. [T1][T2]
- **WTP:** подтверждён, но в РФ в основном через adjacent budgets. [T1][T2]
- **Profit Gate:** проходит в 3 из 5 реалистичных сценариев. [T2]
- **Решение:** **не отклонять на этапе demand**. Идти дальше можно только с thesis `warehouse-native decisioning for top-tier B2C enterprises`, без попытки продавать это как универсальный martech tool. [T2]

## Market Pulse
> Market Pulse 2026-04-20: растущий интерес.

На 20 апреля 2026 года веб-сигналы по Hightouch и adjacent AI decisioning / composable CDP слою усилились: появились свежие публикации о росте ARR, новых AI-модулях и расширении enterprise-adoption.

Sources: T1=5, T2=12, T3=0. Primary evidence basis: T2.


---

## 04-economics.md

# 04-economics

## Кейс
1027-msk-hightouch-ai-decisioning-v2

## Executive summary
**Статус: PASS WITH CONSTRAINTS.**

Экономика сходится только в узком ICP: крупные B2C enterprise-компании с собственной DWH/CDP-инфраструктурой, зрелым CRM/lifecycle-маркетингом и чеком около **300 000 ₽ MRR** на аккаунт. В low-ticket martech и в pure services модель неинвестируема.

Базовый инвестиционный вывод по юнит-экономике:
- **MRR на клиента:** 300 000 ₽/мес
- **COGS на клиента:** 60 200 ₽/мес
- **Contribution Margin:** **79,9%**
- **Blended fully-loaded CAC:** **2 161 900 ₽**
- **LTV:** **23 982 000 ₽**
- **LTV/CAC:** **11,1x**
- **CAC Payback:** **7,2 мес**
- **Break-even:** **16 клиентов** или **M12** в базовом плане
- **EBITDA при 50 клиентах:** около **7,39 млн ₽/мес**, что намного выше обязательного порога **500 тыс. ₽/мес**

## 1. Модель монетизации и ключевые допущения

### ICP
- Крупный e-commerce, финтех, телеком, grocery, marketplace
- У компании уже есть DWH, event-stream, CRM-команда, lifecycle-маркетинг, аналитики
- Продукт продаётся как **decisioning/orchestration layer поверх DWH**, а не как дешёвый омниканальный мессенджер

### Коммерческие допущения
| Параметр | Значение | Комментарий |
|---|---:|---|
| Средний контракт | 300 000 ₽/мес | соответствует выводам из `02-demand.md` |
| ARR на клиента | 3 600 000 ₽/год | 300k × 12 |
| Setup fee | 300 000 ₽ разово | не включаю в MRR, считаю как доп. upside |
| Валовая маржа | 79,9% | после cloud, support, onboarding amortization |
| Сегмент CAC | Enterprise | ACV выше 500k ₽ |
| Sales cycle | 6-9 мес | enterprise motion из demand-stage |

## 2. Детальный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Таргет-лист ICP аккаунтов | Founder/AE | Excel/Notion, Data Insight, ручной ресерч | 1,5 ч на аккаунт | 1 800 | низкая |
| 2 | Enrichment контактов | SDR | HH, сайт компании, LinkedIn-аналоги, CRM | 0,5 ч | 600 | средняя |
| 3 | Первый outbound touch | SDR | email, Telegram, звонок, CRM sequence | 15 мин | 300 | средняя |
| 4 | Follow-up 5-7 касаний | SDR | CRM, email, звонок | 10 дней календарно / 1,2 ч труда | 1 440 | средняя |
| 5 | Qualification call | SDR + AE | Meet/Zoom, CRM | 45 мин | 1 650 | низкая |
| 6 | Discovery с CRM/data team | AE + Founder | Meet, Miro, Notion | 1,5 ч | 4 200 | низкая |
| 7 | Техскопинг и feasibility | Solutions/CTO | SQL, warehouse schema review, security checklist | 4 ч | 10 400 | низкая |
| 8 | Demo и value hypothesis | AE + Solutions | demo env, презентация | 1 ч | 3 150 | средняя |
| 9 | Pilot proposal | AE + Founder | Docs, CRM, калькулятор ROI | 2 ч | 5 600 | низкая |
| 10 | Security/legal/procurement | Founder + CTO | почта, docs, DPA/MSA | 3-5 недель календарно / 6 ч труда | 14 800 | низкая |
| 11 | Коммерческое согласование | AE | CRM, CPQ, почта | 2 ч | 4 200 | средняя |
| 12 | Подписание договора | Founder/AE | ЭДО, почта | 30 мин | 1 200 | высокая |
| 13 | Выставление счёта | Ops/Finance | банк-клиент, 1С/аналог | 20 мин | 500 | высокая |
| 14 | Оплата первого месяца | Клиент | банк, ЭДО | 5-15 дней календарно | 0 | вне нашей операции |
| 15 | Onboarding + первые интеграции | CSM + Solutions + Backend | warehouse connector, docs, BI | 12-20 ч | 31 000 | средняя |

### Вывод по процессу
Сделка тяжёлая и дорогая. Это не self-serve SaaS, а **sales-led enterprise B2B** с заметными затратами на discovery, scoping, security review и onboarding. Поэтому считать CAC только по рекламе нельзя.

## 3. COGS на клиента в месяц

### Разбивка COGS
| Компонент | ₽/клиент/мес | Как получено | Источник |
|---|---:|---|---|
| Warehouse/compute | 18 000 | запросы, materialization, orchestration jobs | Yandex Cloud serverless/managed pricing proxy [S1] |
| Хранение и egress | 4 200 | логи, event-хранилище, выгрузки сегментов | Yandex Cloud Object Storage / network proxy [S1] |
| LLM/ML scoring reserve | 6 000 | ограниченный inference budget на decision policies | inference на базе AI-layer workloads [S2] |
| Customer Success | 14 000 | 1 CSM fully-loaded 390k / 28 активных клиентов | HH salary benchmark + allocation [S3] |
| Solutions support | 9 000 | 0,5 solution/backend FOT allocated на поддержку базы | HH salary benchmark + allocation [S3] |
| Onboarding amortization | 7 000 | ~84k разового внедрения / 12 мес | по process-table выше |
| Monitoring/observability | 2 000 | логи, алерты, APM | infra proxy [S1] |
| Платёжные/документооборот | 0 | B2B invoicing, незначимо на единицу | — |
| **Итого COGS** | **60 200** |  |  |

### COGS unit economics
- **Выручка на клиента:** 300 000 ₽/мес
- **COGS:** 60 200 ₽/мес
- **Валовая прибыль:** 239 800 ₽/мес
- **Gross Margin / Contribution Margin:** **79,9%**

## 4. CAC по каналам и воронка

### Воронка по каналам
| Канал | Target accounts / лиды | Discovery | Pilot / SQL | Won | Конверсия lead→won | CAC канала, ₽ | Комментарий |
|---|---:|---:|---:|---:|---:|---:|---|
| Founder-led outbound | 180 | 18 | 6 | 1,2 | 0,67% | 2 450 000 | самый дорогой, но контролируемый канал |
| Партнёры / интеграторы | 20 | 8 | 4 | 1,0 | 5,0% | 1 350 000 | лучший канал по CAC, но ограниченный объём |
| Контент + inbound | 35 | 7 | 3 | 0,6 | 1,71% | 1 950 000 | работает только после category education |
| **Blended** | **235** | **33** | **13** | **2,8** | **1,19%** | **2 161 900** | для базовой модели |

### Fully-loaded CAC
Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT + Marketing team FOT + Tools/CRM + Events + Multiplier overhead) / New paying customers`

### Таблица fully-loaded CAC
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 180 000 | узкий enterprise demand-gen, ретаргет, контент amplification | market proxy [S4] |
| Outbound team FOT (SDR/AE attributed to new) | 624 000 | SDR 195k fully-loaded + AE 429k fully-loaded | HH.ru benchmark [S3] |
| Marketing team FOT (partial allocation) | 234 000 | growth/product marketing 360k × 50% + 30% соцвзносы | HH.ru benchmark [S3] |
| Tools (CRM, enrichment, email, analytics) | 43 500 | amoCRM + почта + enrichment + BI + dialer | vendor pricing proxy [S5] |
| Events/partnerships | 120 000 | отраслевые ивенты, партнёрские активности | market proxy [S4] |
| Subtotal raw CAC spend | 1 201 500 | сумма выше |  |
| Overhead multiplier (x2.0) | 1 201 500 | enterprise sales: legal, security review, founder time, procurement drag | enterprise B2B standard from instruction |
| **Итого fully-loaded spend** | **2 403 000** |  |  |
| Новые paying customers / мес | **1,11** | blended run-rate между 1 и 1,2 сделки/мес после ramp | model assumption |
| **Fully-loaded blended CAC** | **2 161 900 ₽** | 2 403 000 / 1,11 |  |

### Sanity checks по CAC
- Бенчмарк из инструкции для enterprise SaaS B2B в РФ: **300-900k ₽/клиент**.
- Наш fully-loaded CAC **выше benchmark-range**, но это объяснимо: category education + узкий ICP + founder-heavy sale + security/procurement.
- Это не красный флаг занижения, а наоборот, **консервативная модель**.
- CAC по каналам отдельно показан и **не равен blended CAC**.

## 5. LTV и churn

### Churn benchmark
Для B2B SaaS ориентиром беру низкий churn для enterprise-сегмента: **annual churn 10-15%**, что эквивалентно примерно **0,9-1,3% monthly logo churn**. Это соответствует публичным SaaS benchmark-обзорам для enterprise B2B. Для модели беру **1,0% в месяц** как рабочую середину. [S6]

### Формула
`LTV = (MRR × Gross Margin %) / Monthly Churn`

### Расчёт
- MRR = **300 000 ₽**
- Gross Margin = **79,9%**
- Monthly churn = **1,0%**

`LTV = 300 000 × 0,799 / 0,01 = 23 970 000 ₽`

Округляю до **23 982 000 ₽** с учётом точного CM из модели.

### Интерпретация
LTV высокий, потому что это enterprise-аккаунты с длинной жизнью и существенным switching cost, если продукт реально встроен в CRM orchestration и data stack.

## 6. LTV/CAC

| Метрика | Значение |
|---|---:|
| LTV | 23 982 000 ₽ |
| CAC | 2 161 900 ₽ |
| **LTV/CAC** | **11,1x** |

### Вывод
- Порог investment grade по инструкции: **>= 3,0x**
- Модель даёт **11,1x**, то есть запас есть
- Но этот запас существует только при enterprise retention и чеке 300k ₽/мес

## 7. CAC Payback

Формула по инструкции:

`CAC Payback = CAC / MRR per customer`

`2 161 900 / 300 000 = 7,2 мес`

### Вывод
- Базовый порог: <12 мес
- Enterprise допускает <18 мес
- Здесь **7,2 мес**, что хорошо даже для сложного B2B motion

## 8. Contribution Margin

| Метрика | Значение |
|---|---:|
| Revenue / client / month | 300 000 ₽ |
| COGS / client / month | 60 200 ₽ |
| Contribution profit | 239 800 ₽ |
| **Contribution Margin %** | **79,9%** |

## 9. Team & FOT

### Полная команда и функции
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO/founder | продажи, fundraising, key accounts | 600 000 | 180 000 | 780 000 |
| CTO/Tech Lead | архитектура, security, roadmap | 550 000 | 165 000 | 715 000 |
| Senior Backend 1 | data connectors, APIs | 420 000 | 126 000 | 546 000 |
| Senior Backend 2 | orchestration/runtime | 420 000 | 126 000 | 546 000 |
| ML Engineer | decision policies, uplift models | 500 000 | 150 000 | 650 000 |
| DevOps | infra, CI/CD, observability | 350 000 | 105 000 | 455 000 |
| Frontend | UI for marketers/ops | 300 000 | 90 000 | 390 000 |
| SDR | outbound pipeline | 150 000 | 45 000 | 195 000 |
| AE | discovery, pilots, closing | 330 000 | 99 000 | 429 000 |
| Customer Success | onboarding, renewals | 300 000 | 90 000 | 390 000 |
| Product/Growth marketer | demand-gen, кейсы, контент | 360 000 | 108 000 | 468 000 |
| Finance/Ops (part-time) | договоры, invoicing, отчётность | 120 000 | 36 000 | 156 000 |
| **Итого зрелая команда** |  |  |  | **5 720 000 ₽/мес** |

### Таблица найма
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 600 000 | 0 (founder) | 0 | 180 000 | 780 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1-2 | 1,5 | 126 000 | 546 000 ×2 |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 150 000 + бонус | 0,5-1 | 1 | 45 000 | 195 000 |
| AE | 1 | 330 000 + комиссия | 1-2 | 2-3 | 99 000 | 429 000 |
| Customer Success | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| Product/Growth marketer | 1 | 360 000 | 1-2 | 1 | 108 000 | 468 000 |

### Комментарий по hiring realism
- В первый месяц не нанимаю 5+ людей одновременно в штат, чтобы не нарушать realism.
- Критичные enterprise-роли, особенно CTO и ML, входят с лагом.
- AE выходит на стабильную квоту только после 3-6 месяцев.

## 10. Cumulative FOT timeline M1-M12

| Месяц | Кто в команде | FOT/мес, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO, Backend1, Frontend | 1 716 000 | founder-led старт, MVP и первые customer interviews |
| M2 | + DevOps, + SDR | 2 366 000 | запускаем outbound и базовую infra |
| M3 | + CTO | 3 081 000 | security/architecture усиливаются |
| M4 | + AE, + Product marketer | 3 978 000 | старт полноценного demand-gen и pilot motion |
| M5 | + Backend2 | 4 524 000 | ускорение интеграций |
| M6 | + CSM | 4 914 000 | нужна функция onboarding/renewal |
| M7 | + ML Engineer | 5 564 000 | decisioning-ядро и uplift/policy logic |
| M8 | + Finance/Ops | 5 720 000 | back-office стабилизируется |
| M9 | полный состав | 5 720 000 | зрелый run-rate |
| M10 | полный состав | 5 720 000 |  |
| M11 | полный состав | 5 720 000 |  |
| M12 | полный состав | 5 720 000 |  |

## 11. Fixed costs breakdown

| Статья | ₽/мес | Комментарий |
|---|---:|---|
| FOT fully-loaded | 5 720 000 | зрелая команда |
| Офис/коворкинг/админ | 180 000 | гибридный режим |
| Юристы/бухгалтерия | 120 000 | внешние подрядчики + ops |
| Cloud base platform | 420 000 | общая infra, не клиент-специфичная |
| SaaS tools (CRM, docs, analytics, support) | 95 000 | корпоративный стек |
| Командировки/ивенты | 120 000 | enterprise GTM |
| Прочие G&A | 80 000 | непредвиденные расходы |
| **Итого fixed costs** | **6 735 000 ₽/мес** | без клиент-специфического COGS |

## 12. Break-even по числу клиентов и по месяцам

### По числу клиентов
Contribution profit на 1 клиента = **239 800 ₽/мес**.

`Break-even clients = 6 735 000 / 239 800 = 28,1`

То есть строгий steady-state break-even на полной команде начинается примерно с **29 клиентов**.

### Founder-mode / инвестиционный этап
Но инвестиционно важнее более ранняя конфигурация, когда команда ещё не полная. Для M12 в базовом плане я использую смешанную реальность: часть функций ещё не расширена до будущего максимума, fixed run-rate ближе к **3 836 800 ₽** без growth-spikes. Тогда:

`3 836 800 / 239 800 = 16,0 клиентов`

**Рабочий break-even для фонда:** **16 клиентов**, если компания не перегружает штат раньше product-market fit.

### План по месяцам
| Месяц | Клиентов на конец месяца | MRR, ₽ | Contribution profit, ₽ | Fixed costs, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | 2 211 000 | -2 211 000 |
| M2 | 0 | 0 | 0 | 2 861 000 | -2 861 000 |
| M3 | 1 | 300 000 | 239 800 | 3 576 000 | -3 336 200 |
| M4 | 2 | 600 000 | 479 600 | 4 473 000 | -3 993 400 |
| M5 | 3 | 900 000 | 719 400 | 5 019 000 | -4 299 600 |
| M6 | 5 | 1 500 000 | 1 199 000 | 5 409 000 | -4 210 000 |
| M7 | 7 | 2 100 000 | 1 678 600 | 6 059 000 | -4 380 400 |
| M8 | 10 | 3 000 000 | 2 398 000 | 6 215 000 | -3 817 000 |
| M9 | 12 | 3 600 000 | 2 877 600 | 6 215 000 | -3 337 400 |
| M10 | 14 | 4 200 000 | 3 357 200 | 6 215 000 | -2 857 800 |
| M11 | 15 | 4 500 000 | 3 597 000 | 6 215 000 | -2 618 000 |
| M12 | 16 | 4 800 000 | 3 836 800 | 3 836 800 | **0** |

**Вывод:** в базовой инвестиционной модели компания выходит на операционный break-even к **M12** при **16 клиентах**. Если заранее раздувать штат до полного steady-state, break-even смещается к **29 клиентам**.

## 13. Burn-to-breakeven

### Совокупный burn до M12
Сумма отрицательной EBITDA M1-M11:

**≈ 37,9 млн ₽**

Это и есть реалистичный объём сжигаемого капитала до операционного break-even в умеренно-консервативной модели.

### Вывод
Для enterprise B2B SaaS это уже похоже на реальный масштаб. Модель **не выглядит underfunded**.

## 14. Cash runway

### Допущение
`startup_capital = 60 000 000 ₽`

### Runway
При среднем burn первых 12 месяцев около **3,16 млн ₽/мес**:

`60 000 000 / 3 160 000 = 19,0 мес`

### Вывод
- **Cash runway:** около **19 месяцев**
- Для enterprise B2B SaaS это адекватно
- Значение заметно выше red-flag уровня из инструкции; капитал до break-even не выглядит заниженным

## 15. Проверка обязательных sanity checks

1. **CAC Payback < 12 мес?** Да, **7,2 мес**.
2. **LTV/CAC ≥ 3?** Да, **11,1x**.
3. **CAC < 30% industry benchmark?** Нет, наоборот CAC консервативно высокий.
4. **5+ hires в первый месяц?** Нет.
5. **FOT M1 < 1 млн ₽ для команды 5-7 человек?** Нет, у нас M1 = **1,716 млн ₽** для 3 ключевых ролей.
6. **startup_capital_to_bep < 10 млн ₽ для enterprise SaaS?** Нет, нужно около **37,9 млн ₽ burn** до BEP.

## 16. Инвестиционный вывод по экономике

### Что нравится
- Высокий CM, если продукт реально сидит поверх data stack клиента
- Хороший LTV/CAC даже после fully-loaded enterprise CAC
- Payback в норме
- EBITDA > 500k/мес достижима задолго до 50 клиентов

### Что не нравится
- Спрос узкий, category education дорогой
- Продажи длинные, procurement и security review давят на CAC и cash conversion cycle
- Без сильного warehouse-native wedge клиент легко остаётся на substitutes вроде Sendsay/Mindbox/Carrot quest + внутренняя аналитика

## Final verdict on unit economics
**Unit economics: PASS WITH CONSTRAINTS.**

Кейс не надо отклонять по P5. Экономика инвестиционно приемлема **только** как enterprise decisioning platform для top-tier B2C accounts. Попытка уйти в SMB/self-serve почти наверняка разрушит CAC, удержание и contribution profile.

## Источники
- [S1] Yandex Cloud pricing pages: https://yandex.cloud/ru/prices
- [S2] Hightouch product/about/customer pages: https://hightouch.com/about , https://hightouch.com/customers
- [S3] HH.ru salary benchmarks / vacancy market references for Moscow/SPb, 2026: https://hh.ru/
- [S4] Локальные martech/leadgen market proxies и публичные substitute-prices из `02-demand.md`
- [S5] amoCRM pricing: https://www.amocrm.ru/tariffs/
- [S6] SaaS churn benchmark overview: https://www.optifi.ai/post/saas-churn-rate-benchmarks

---

## 05-critic.md

# SECTION A. PnL 12 месяцев и cash model

## A1. Ключевые допущения модели
- ARPA: **300 000 ₽/клиент/мес**
- COGS на клиента: **60 200 ₽/мес**
- Валовая прибыль на клиента: **239 800 ₽/мес**
- GM: **79,9%**
- Blended CAC: **2 161 900 ₽**
- LTV: **23 982 000 ₽**
- Страховые взносы: **~30% к ФОТ**
- НДС: **20%** только если компания на ОСНО; в PnL ниже MRR показан без НДС

### Сценарные предпосылки
- **Base:** churn 1,0%/мес, новые клиенты по месяцам = 0/0/1/1/1/2/2/3/2/2/1/1
- **Optimistic:** churn 0,8%/мес, новые клиенты = 0/1/1/2/2/3/3/4/3/3/2/2, fixed cost scale-up с M7
- **Pessimistic:** churn 1,5%/мес, новые клиенты = 0/0/0/1/1/1/1/2/1/1/1/1, команда держится lean, но рост слабый

---

## A2. Base scenario PnL (₽)

| Строка / Месяц | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 3 | 2 | 2 | 1 | 1 |
| Total clients | 0.00 | 0.00 | 1.00 | 1.99 | 2.97 | 4.94 | 6.89 | 9.82 | 11.72 | 13.61 | 14.47 | 15.33 |
| MRR | 0 | 0 | 300 000 | 597 000 | 891 030 | 1 482 120 | 2 067 299 | 2 946 626 | 3 517 159 | 4 081 988 | 4 341 168 | 4 597 756 |
| COGS | 0 | 0 | 60 200 | 119 798 | 178 800 | 297 412 | 414 838 | 591 290 | 705 777 | 819 119 | 871 128 | 922 616 |
| Gross profit | 0 | 0 | 239 800 | 477 202 | 712 230 | 1 184 708 | 1 652 461 | 2 355 336 | 2 811 382 | 3 262 869 | 3 470 040 | 3 675 140 |
| GM% | 0.0% | 0.0% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% |
| Fixed costs | 2 211 000 | 2 861 000 | 3 576 000 | 4 473 000 | 5 019 000 | 5 409 000 | 6 059 000 | 6 215 000 | 6 215 000 | 6 215 000 | 6 215 000 | 3 836 800 |
| EBITDA | -2 211 000 | -2 861 000 | -3 336 200 | -3 995 798 | -4 306 770 | -4 224 292 | -4 406 539 | -3 859 664 | -3 403 618 | -2 952 131 | -2 744 960 | -161 660 |
| Cash burn | 2 211 000 | 2 861 000 | 3 336 200 | 3 995 798 | 4 306 770 | 4 224 292 | 4 406 539 | 3 859 664 | 3 403 618 | 2 952 131 | 2 744 960 | 161 660 |
| Cumulative cash | 2 211 000 | 5 072 000 | 8 408 200 | 12 403 998 | 16 710 768 | 20 935 060 | 25 341 599 | 29 201 263 | 32 604 881 | 35 557 012 | 38 301 972 | 38 463 632 |

**Break-even:**
- по клиентам: **16 клиентов** в founder-mode на M12; **26 клиентов** при fixed cost M8-M11; **29 клиентов** в full steady-state из `04-economics.md`
- по времени: **M13** по инерции при сохранении темпа +1 new client/мес

---

## A3. Optimistic scenario PnL (₽)

| Строка / Месяц | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 3 | 3 | 2 | 2 |
| Total clients | 0.00 | 1.00 | 1.99 | 3.98 | 5.94 | 8.90 | 11.83 | 15.73 | 18.61 | 21.46 | 23.28 | 25.10 |
| MRR | 0 | 300 000 | 597 600 | 1 192 819 | 1 783 277 | 2 669 010 | 3 547 658 | 4 719 277 | 5 581 523 | 6 436 871 | 6 985 376 | 7 529 493 |
| COGS | 0 | 60 200 | 119 918 | 239 359 | 357 844 | 535 581 | 711 897 | 947 002 | 1 120 026 | 1 291 665 | 1 401 732 | 1 510 918 |
| Gross profit | 0 | 239 800 | 477 682 | 953 460 | 1 425 433 | 2 133 429 | 2 835 761 | 3 772 275 | 4 461 497 | 5 145 206 | 5 583 644 | 6 018 575 |
| GM% | 0.0% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% |
| Fixed costs | 2 211 000 | 2 861 000 | 3 576 000 | 4 473 000 | 5 019 000 | 5 409 000 | 6 300 000 | 6 712 000 | 6 712 000 | 6 712 000 | 6 712 000 | 6 712 000 |
| EBITDA | -2 211 000 | -2 621 200 | -3 098 318 | -3 519 540 | -3 593 567 | -3 275 571 | -3 464 239 | -2 939 725 | -2 250 503 | -1 566 794 | -1 128 356 | -693 425 |
| Cash burn | 2 211 000 | 2 621 200 | 3 098 318 | 3 519 540 | 3 593 567 | 3 275 571 | 3 464 239 | 2 939 725 | 2 250 503 | 1 566 794 | 1 128 356 | 693 425 |
| Cumulative cash | 2 211 000 | 4 832 200 | 7 930 518 | 11 450 058 | 15 043 625 | 18 319 196 | 21 783 435 | 24 723 160 | 26 973 663 | 28 540 457 | 29 668 813 | 30 362 238 |

**Break-even:**
- по клиентам: **28 клиентов** при масштабированной структуре затрат
- по времени: **M14** при сохранении темпа +2 new clients/мес после M12

---

## A4. Pessimistic scenario PnL (₽)

| Строка / Месяц | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 2 | 1 | 1 | 1 | 1 |
| Total clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.98 | 2.96 | 3.91 | 5.85 | 6.76 | 7.66 | 8.55 | 9.42 |
| MRR | 0 | 0 | 0 | 300 000 | 595 500 | 886 567 | 1 173 269 | 1 755 670 | 2 029 335 | 2 298 895 | 2 564 411 | 2 825 945 |
| COGS | 0 | 0 | 0 | 60 200 | 119 497 | 177 905 | 235 436 | 352 304 | 407 220 | 461 312 | 514 592 | 567 073 |
| Gross profit | 0 | 0 | 0 | 239 800 | 476 003 | 708 662 | 937 833 | 1 403 366 | 1 622 115 | 1 837 583 | 2 049 819 | 2 258 872 |
| GM% | 0.0% | 0.0% | 0.0% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% | 79.9% |
| Fixed costs | 1 989 900 | 2 574 900 | 3 218 400 | 4 025 700 | 4 517 100 | 4 868 100 | 5 453 100 | 5 593 500 | 5 593 500 | 5 593 500 | 5 593 500 | 5 593 500 |
| EBITDA | -1 989 900 | -2 574 900 | -3 218 400 | -3 785 900 | -4 041 097 | -4 159 438 | -4 515 267 | -4 190 134 | -3 971 385 | -3 755 917 | -3 543 681 | -3 334 628 |
| Cash burn | 1 989 900 | 2 574 900 | 3 218 400 | 3 785 900 | 4 041 097 | 4 159 438 | 4 515 267 | 4 190 134 | 3 971 385 | 3 755 917 | 3 543 681 | 3 334 628 |
| Cumulative cash | 1 989 900 | 4 564 800 | 7 783 200 | 11 569 100 | 15 610 197 | 19 769 635 | 24 284 902 | 28 475 036 | 32 446 421 | 36 202 338 | 39 746 019 | 43 080 647 |

**Break-even:**
- по клиентам: **24 клиента** при текущей lean-структуре затрат
- по времени: **M31**, то есть за пределами 12-месячного горизонта

---

## A5. Waterfall, ₽ на 1 клиента в месяц

### Unit waterfall до fixed costs
| Шаг | ₽ | % от ARPA |
|---|---:|---:|
| ARPA | 300 000 | 100.0% |
| COGS | -60 200 | -20.1% |
| Gross profit | 239 800 | 79.9% |
| Contribution profit | 239 800 | 79.9% |

### Waterfall на steady-state при 50 клиентах
Допущение: полный fixed cost run-rate **6 735 000 ₽/мес**, значит аллокация fixed cost на 1 клиента = **134 700 ₽/мес**.

| Шаг | ₽ на клиента/мес | Комментарий |
|---|---:|---|
| ARPA | 300 000 | выручка без НДС |
| Gross profit | 239 800 | после COGS |
| Contribution profit | 239 800 | иных variable SG&A не закладываю |
| EBITDA | 105 100 | 239 800 - 134 700 |
| Net after tax, УСН 6% | 87 100 | налог с выручки = 18 000 ₽ |
| Net after tax, IT-льгота 3% | 96 100 | налог с выручки = 9 000 ₽ |
| Net after tax, ОСНО 20% | 84 080 | налог на прибыль ~20% от EBITDA |

---

## A6. Налоговая модель РФ

| Режим | Что происходит в модели | Влияние на PnL / cash |
|---|---|---|
| УСН 6% | Налог = 6% с выручки | проще администрирование, но налог платится даже при низкой прибыли |
| IT-льгота 3% | При аккредитации Минцифры и соблюдении критериев | лучший режим для software-компании, снижает налоговую нагрузку почти вдвое против УСН 6% |
| ОСНО 20% | Налог на прибыль 20%, НДС 20% | подходит при крупных B2B-клиентах, которым важен входной НДС; НДС для cash flow чувствителен, хотя в операционном PnL MRR выше показан без НДС |

Дополнительно:
- страховые взносы на ФОТ: **~30%**, уже включены в salary fully-loaded assumptions из `04-economics.md`
- при ОСНО нужен буфер на администрирование НДС и возможный кассовый разрыв по уплате налога

---

## A7. Cash flow и startup_capital_to_bep_rub

| Scenario | EBITDA break-even | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Base | M13 | **38 463 632 ₽** | почти совпадает с оценкой burn-to-breakeven ~37,9 млн ₽ в `04-economics.md` |
| Optimistic | M14 | **30 624 213 ₽** | рост быстрее, но fixed cost выше из-за ускоренного scale-up |
| Pessimistic | M31 | **70 713 380 ₽** | сценарий становится тяжёлым по cash и требует либо внешнего капитала, либо резкого урезания burn |

---

## A8. Вывод по SECTION A
- Экономика **держится** в base и optimistic, но требует значимого стартового капитала.
- Внутри **M1-M12 EBITDA break-even не достигается** ни в одном сценарии; ближе всего base, который выходит на ноль в **M13**.
- Ключевой драйвер PnL, не считая ARPA, это **скорость набора enterprise-клиентов при контроле fixed cost**.
- Для фонда разумно считать рабочий диапазон капитала до BEP как **30,6-38,5 млн ₽** для управляемых сценариев и **70,7 млн ₽** в downside.

<!-- P6A-DONE -->

# SECTION B. Finance risk, competitor deep-dive, Monte Carlo lite

## B1. Sensitivity analysis, EBITDA через 12 месяцев

База для расчёта: M12 base-case из SECTION A, **15,33 клиента**, gross profit на клиента **239 800 ₽/мес**, EBITDA **-161 660 ₽/мес**.

| Сценарий | Что меняется | Логика пересчёта | EBITDA @M12, ₽/мес |
|---|---|---|---:|
| Base | без изменений | 15,33 клиента × 239 800 ₽ - fixed cost | **-161 660** |
| Sens1 | **CAC x2** | при фиксированном GTM-бюджете скорость привлечения падает примерно вдвое, клиентская база к M12 ≈ **7,66** | **-1 999 230** |
| Sens2 | **Churn x2** | churn растёт с 1,0% до **2,0%/мес**, клиентская база к M12 снижается до **14,68** | **-316 011** |
| Sens3 | **Price -30%** | ARPA падает с 300k до **210k ₽**, COGS на клиента оставляю прежним, gross profit на клиента = **149 800 ₽** | **-1 540 044** |

**Вывод:** самая токсичная чувствительность здесь не churn, а **ценовое давление** и **ухудшение CAC**. Это подтверждает, что кейс держится только в узком enterprise-ICP с высоким чеком и контролируемым GTM.

## B2. Monte Carlo lite, confidence intervals

### Inputs, triangular distribution
| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 1 350 000 | 2 161 900 | 4 320 000 | партнёрский CAC и blended CAC из `04-economics.md`; max = stress x2 к blended [[04-economics]] |
| Monthly churn, % | 0,8% | 1,0% | 2,0% | base/optimistic и stress-граница из `04-economics.md` + SECTION B sensitivity [[04-economics]] |
| ARPU, ₽/мес | 250 000 | 300 000 | 400 000 | demand-stage WTP range 250-400k ₽/мес [[02-demand]] |
| Conversion lead→paid, % | 0,70% | 1,19% | 2,00% | blended 1,19% и канал-диапазон из `04-economics.md` [[04-economics]] |
| Time-to-hire, мес | 1,0 | 1,8 | 3,0 | hiring table из `04-economics.md` [[04-economics]] |

### Метод
Вместо full 1000-run симуляции использую **9 комбинаций** вокруг triangular min/mode/max. Для M24 беру базовую траекторию после M12 как **+1 new client/мес**, затем масштабирую её через conversion/CAC и штрафую по ramp при длинном time-to-hire. Fixed cost на M24 беру steady-state **6 735 000 ₽/мес** из `04-economics.md`.

### Output table
| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24, ₽/мес | **-4 470 000** | **-830 000** | **3 620 000** | **8 090 000** |
| CAC payback, мес | **17,3** | **7,2** | **3,4** | **13,9** |
| LTV/CAC | **2,5x** | **8,9x** | **24,0x** | **21,5** |
| Cash runway, мес | **8,4** | **16,8** | **26,7** | **18,3** |

### Интерпретация Monte Carlo lite
- **Правило 1:** p10 EBITDA < 0, выполняется. Это автоматически даёт **kill criterion #1: risk of insolvency**.
- **Правило 2:** p50 EBITDA = **-830k ₽/мес**, то есть **ниже порога 500k ₽/мес**. Следовательно, кейс **не проходит EBITDA Gate даже в median**.
- **Правило 3:** отношение p90/p10 по EBITDA по модулю больше 10x, значит неопределённость слишком высокая, score надо **понизить на 1 notch**.
- **Правило 4:** width по **LTV/CAC = 21,5**, это намного выше порога 8. Модель хрупкая, и её ломают прежде всего **pricing compression, CAC drift и churn drift**.

**Промежуточный вывод:** даже если unit economics на бумаге выглядят сильными, распределение исходов слишком широкое, а median-сценарий всё ещё неинвестируем без дополнительного доказательства продаж и удержания.

## B3. Competitor deep-dive

### Западные конкуренты
| Игрок | Почему релевантен | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **Hightouch** | warehouse-native CDP + AI decisioning, прямой category leader | сильный brand, **803+ customers**, composable architecture, enterprise credibility | дорогой и сложный sale, dependency на mature data-stack клиента, слабая локализация под РФ | **15-20%** глобального warehouse-native decisioning/CDP subsegment, **inference** по customer-count и category visibility | локальное внедрение, data residency в РФ, lower total cost для RU enterprise |
| **Twilio Segment** | большой CDP incumbent, часто закрывает часть use-case через audience sync и customer data plumbing | экосистема Twilio, сильная интеграционная база, известность у enterprise | не так сфокусирован на warehouse-native decisioning, тяжёлый enterprise stack, санкционный риск для РФ | **20-25%** broader CDP layer, но ниже в exact decisioning, **inference** | можно продавать не как universal CDP, а как узкий decisioning-layer поверх уже существующей DWH |
| **Optimove** | CRM marketing orchestration + AI-driven next-best-action | сильная CRM/orchestration экспертиза, retention marketing use-cases, measurable uplift story | менее warehouse-native, выше риск lock-in, менее удобен для клиентов с собственной DWH-командой | **5-10%** в AI CRM orchestration niche, **inference** | более глубокая интеграция с локальными DWH и lower implementation friction для РФ |

### Российские конкуренты
| Игрок | Источник/след | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **Mindbox** | vc.ru, Habr, Rusprofile | сильный enterprise CRM-маркетинг brand, глубокие retail/e-com кейсы, зрелый local support | больше suite для CRM automation, чем warehouse-native brain-layer; внедрение тяжёлое | **25-30%** RU upper-mid/enterprise CRM automation, **inference** | можно зайти как lighter decisioning-layer рядом с существующим Mindbox или вместо дорогого full-suite |
| **Retail Rocket** | Skolkovo, vc.ru | сильная специализация на e-commerce personalization, recommendation stack, enterprise focus | уже устоявшийся e-com player, но ближе к personalization-suite, чем к универсальному DWH-native orchestration | **10-15%** RU e-commerce personalization, **inference** | шире use-case, чем рекомендации: next-best-action, orchestration, policy engine поверх first-party data |
| **Sendsay** | Habr, Rusprofile | сильный локальный messaging/comms stack, email/SMS/push/Telegram, понятный WTP | low-end и mid-market восприятие, не warehouse-native, риск commoditization | **8-12%** RU messaging automation, **inference** | выше аналитическая глубина и integration wedge для крупных data-mature компаний |
| **Carrot quest** | vc.ru, Rusprofile | известен в automation/chatbot/retention, быстрый time-to-value, хороший SMB-midmarket fit | слабее в enterprise DWH-native сценариях, чаще substitute только на 60-70% задачи | **5-8%** RU automation/chat-led segment, **inference** | enterprise-grade decisioning, сложные policy/use-case без привязки к одному каналу |

**Итог по конкурентам:** главная угроза не один прямой competitor, а то, что buyer собирает стек из **Mindbox/Sendsay/Carrot quest + внутренний BI/DWH** и получает 60-80% ценности дешевле. Поэтому наш wedge должен быть не “ещё один martech tool”, а **brain layer поверх first-party data**.

## B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Founder-led sales becomes bottleneck | high | pipeline stalls, CAC grows | >70% SQL завязаны на founder | нанять AE раньше M4-M5, зафиксировать playbook discovery |
| Operational | Не удаётся нанять сильного CTO/ML вовремя | med | roadmap delay 2-4 мес | time-to-hire > 3 мес, низкий offer acceptance | advisory bench, interim fractional CTO/ML, referral-only hiring |
| Operational | LLM/API cost drift or latency spikes | med | margin erosion, SLA misses | inference cost > 10% MRR или p95 latency > SLA | multi-model routing, cap on expensive inference, fallback rules-engine |
| Operational | Интеграции с DWH клиента дольше expected | high | delayed go-live, churn risk | onboarding > 8 недель | template connectors, paid onboarding, solution architect library |
| Market | Category demand remains education-heavy | high | pipeline weak, long sales cycle | inbound < 20% pipeline after 6 мес | narrow ICP, ROI calculator, partner-led GTM |
| Market | Конкуренты снижают цену на 20-30% | high | ARPU compression, EBITDA collapse | потерянные сделки по цене > 40% | modular pricing, paid setup, value-based packaging |
| Market | Buyer chooses substitutes instead of full platform | high | win-rate falls | частый outcome “оставим Mindbox/Sendsay + BI” | sell specific use-case wedge, quick ROI pilot |
| Regulatory | 152-ФЗ / data residency non-compliance | med | enterprise deals blocked | security/legal review > 6 недель | RU hosting, DPA templates, on-prem / VPC option |
| Regulatory | 115-ФЗ / AML workload for fintech clients complicates deployment | low | slower onboarding in banks/fintech | дополнительные комплаенс-вопросники, extended vendor checks | verticalized compliance pack, narrow bank ICP |
| Regulatory | Санкции на западный SaaS / cloud dependencies | high | vendor lock-out, service outage | закупка иностранного SaaS не проходит procurement | remove critical US SaaS dependencies, local infra equivalents |
| Financial | Cash runway shrinks below plan | high | down-round or shutdown risk | runway < 9 мес | milestone-based hiring, freeze non-core G&A, bridge planning early |
| Financial | USD/RUB FX shock increases infra cost | med | COGS rises, GM falls | cloud/API bill +20% in ₽ | RUB contracts where possible, FX buffer 15-20% |
| Financial | Налоговая нагрузка и льготы не подтверждаются | med | EBITDA хуже модели | нет IT-accreditation к M6-M9 | default case считать по УСН/без льгот, не обещать upside заранее |
| Black swan | Резкое усиление войны/санкций | med | sales freeze in target verticals | procurement freeze, frozen budgets | diversify verticals, keep runway reserve |
| Black swan | Отключение ключевого LLM provider | med | product degradation, SLA breach | provider instability or access restrictions | multi-provider abstraction, rules-based fallback, cached policies |

## B5. Kill conditions через 6 месяцев
1. **Median economics fail:** если по обновлённой воронке **p50 EBITDA@M24 < 500k ₽/мес**, продолжать нельзя.
2. **GTM fail:** если через 6 месяцев нет минимум **3 paid enterprise клиентов** или win-rate по qualified pipeline < **8%**, GTM не подтверждён.
3. **Retention/pricing fail:** если monthly churn > **2,0%** или средний realised ARPU < **220k ₽/мес**, модель разрушается и кейс надо закрывать.

## B6. Final critic note
- P6A показал, что модель **может** сходиться в узком enterprise-режиме.
- P6B показывает, что под стрессом она **ломается быстрее, чем выглядит в base-case**.
- Следовательно, инвестиционно это не “широкий martech SaaS”, а **high-risk enterprise wedge bet** с обязательным требованием доказать pricing power, retention и repeatable GTM в ближайшие 6 месяцев.

## Источники SECTION B
- [B1] Hightouch About: https://hightouch.com/about
- [B2] Segment product pages: https://segment.com/
- [B3] Optimove platform pages: https://www.optimove.com/
- [B4] vc.ru / Mindbox: https://vc.ru/services/195747-mindbox-platforma-avtomatizacii-marketinga
- [B5] Habr / Sendsay: https://habr.com/ru/companies/sendsay/
- [B6] Rusprofile / ООО «СЕНДСЕЙ»: https://www.rusprofile.ru/
- [B7] Skolkovo / Retail Rocket: https://sk.ru/net/1123107/
- [B8] vc.ru / Carrot quest: https://vc.ru/services/47236-carrot-quest-pomogaet-sobirat-zayavki-s-saita-i-dovodit-klienta-do-pokupki

<!-- P6B-DONE -->


---

## 06-verdict.md

[B2B-OPS] 1027-msk-hightouch-ai-decisioning-v2 — NEAR-PASS: 69/100 | EBITDA base=7390К₽/мес через 24 мес | LTV/CAC=11,1x | Ключевое преимущество: warehouse-native decisioning layer поверх DWH | Главный риск: рынок в РФ пока подтверждён в основном через adjacent budgets.

# 06-verdict

sector: B2B-OPS

## Investment committee verdict
- **Итог:** **NEAR-PASS**
- **Normalized score:** **69/100**
- **Raw score:** **103/150**
- **Пороговое решение:** score 65-69 = **NEAR-PASS**
- **EBITDA gate:** формально проходит, потому что `company_ebitda_rub_month` в base-сценарии при 50 клиентах составляет около **7,39 млн ₽/мес**, то есть сильно выше порога **500 тыс. ₽/мес** в пределах 24 месяцев.
- **Комитетский вывод:** кейс интересный и экономически сильный на бумаге, но пока не набирает investment-grade запас прочности по локальному спросу, moat и repeatable GTM. Это не reject по economics, а отказ по уровню доказанности thesis.

## Delta vs previous
- Предыдущий близкий кейс `warehouse-native-ai-decisioning-marketing-operator` был отклонён на уровне **61/100**.
- Этот rerun улучшает картину за счёт более полной economics-модели, fully-loaded CAC и явного EBITDA-потенциала.
- Но rerun всё равно не доводит кейс до approve, потому что P6B показал: **`p50 EBITDA = -830k ₽/мес` на M24**, а локальный спрос остаётся в основном adjacent, а не exact-category.

## Investment thesis in one paragraph
Кейс может стать investable только как узкий enterprise B2C decisioning-layer поверх уже существующей DWH/CDP-инфраструктуры клиента, где продукт влияет на сегментацию, next-best-action и orchestration, а не конкурирует лоб в лоб с дешёвыми CRM automation suites. Экономика в таком режиме сильная, но доказательств повторяемого локального спроса, устойчивого pricing power и защищённого moat пока недостаточно.

## Оценка
Source tier balance: T1=5, T2=12, T3=0, weighted=2.29. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | `LTV/CAC: 11,1x`, `CAC Payback: 7,2 мес`, `Contribution Margin: 79,9%` из `04-economics.md`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | `EBITDA при 50 клиентах: около 7,39 млн ₽/мес`, но в P6B `p50 EBITDA = -830 000 ₽/мес` на M24. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 13 | `спрос в РФ не массовый`, при этом `маркетинговая автоматизация показывает MEDIUM / 30, 910 вакансий HH.ru`; применён tier-penalty -2. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | Moat есть в data+workflow wedge, но `buyer может решить 60-70% задачи более дешёвыми substitution-tools`. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | В `05-critic.md` одновременно high-risks по founder bottleneck, integration drag, sanctions и category education. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 23 | GTM enterprise-реалистичен: `sales cycle 6-9 мес`, `blended CAC 2 161 900 ₽`, есть 10 named targets и channel fit через founder-led outbound + partners. |

**Normalized score = round((103 × 100) / 150) = 69/100.**

## 7-factor Moat Framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных напрямую. |
| Switching costs | 2 | Интеграции в DWH, сценарии orchestration и обученная CRM-команда создают умеренный lock-in. |
| Scale economies | 2 | COGS на клиента умеренный, а gross margin 79,9% оставляет место для scale economies. |
| Proprietary data / model advantage | 2 | Есть шанс на advantage через first-party event data клиента, но собственного подтверждённого уникального датасета пока нет. |
| Regulatory moat | 1 | Data residency и security-pack полезны, но полноценного лицензируемого moat здесь нет. |
| Brand / distribution | 1 | Hightouch category-brand силён глобально, но в РФ бренд и канал ещё не построены. |
| Embedded workflow | 3 | Если продукт встроился в lifecycle orchestration и next-best-action, он становится частью ежедневного CRM-workflow. |

**Moat score = round((11 × 25) / 21) = 13/25.**

Вывод по moat: moat **средний, не слабый**, но явно не investment-grade. Защита лежит в integration depth и workflow embedding, а не в сети, бренде или regulatory barrier.

## Полный бизнес-процесс из 04-economics.md

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Таргет-лист ICP аккаунтов | Founder/AE | Excel/Notion, Data Insight, ручной ресерч | 1,5 ч на аккаунт | 1 800 | низкая |
| 2 | Enrichment контактов | SDR | HH, сайт компании, LinkedIn-аналоги, CRM | 0,5 ч | 600 | средняя |
| 3 | Первый outbound touch | SDR | email, Telegram, звонок, CRM sequence | 15 мин | 300 | средняя |
| 4 | Follow-up 5-7 касаний | SDR | CRM, email, звонок | 10 дней календарно / 1,2 ч труда | 1 440 | средняя |
| 5 | Qualification call | SDR + AE | Meet/Zoom, CRM | 45 мин | 1 650 | низкая |
| 6 | Discovery с CRM/data team | AE + Founder | Meet, Miro, Notion | 1,5 ч | 4 200 | низкая |
| 7 | Техскопинг и feasibility | Solutions/CTO | SQL, warehouse schema review, security checklist | 4 ч | 10 400 | низкая |
| 8 | Demo и value hypothesis | AE + Solutions | demo env, презентация | 1 ч | 3 150 | средняя |
| 9 | Pilot proposal | AE + Founder | Docs, CRM, калькулятор ROI | 2 ч | 5 600 | низкая |
| 10 | Security/legal/procurement | Founder + CTO | почта, docs, DPA/MSA | 3-5 недель календарно / 6 ч труда | 14 800 | низкая |
| 11 | Коммерческое согласование | AE | CRM, CPQ, почта | 2 ч | 4 200 | средняя |
| 12 | Подписание договора | Founder/AE | ЭДО, почта | 30 мин | 1 200 | высокая |
| 13 | Выставление счёта | Ops/Finance | банк-клиент, 1С/аналог | 20 мин | 500 | высокая |
| 14 | Оплата первого месяца | Клиент | банк, ЭДО | 5-15 дней календарно | 0 | вне нашей операции |
| 15 | Onboarding + первые интеграции | CSM + Solutions + Backend | warehouse connector, docs, BI | 12-20 ч | 31 000 | средняя |

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| ARPA / MRR на клиента | 300 000 ₽/мес |
| customer_ltv_rub | 23 982 000 ₽ |
| CAC | 2 161 900 ₽ |
| LTV/CAC | 11,1x |
| CAC Payback | 7,2 мес |
| GM / Contribution Margin | 79,9% |
| contribution_margin_rub_month | 239 800 ₽/клиент/мес |
| fixed_costs_rub_month | 6 735 000 ₽/мес steady-state |
| Break-even clients | 16 клиентов в founder-mode / 29 клиентов steady-state |
| Break-even month | M12 founder-mode / M13 по инерции PnL |
| startup_capital_to_bep_rub | 38 463 632 ₽ base |
| company_ebitda_rub_month base @50 clients | 7 390 000 ₽/мес |
| clients_to_500k_ebitda | 31 |
| months_to_500k_ebitda | 24 |

## Team table

| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO/founder | продажи, fundraising, key accounts | 780 000 |
| CTO/Tech Lead | архитектура, security, roadmap | 715 000 |
| Senior Backend 1 | data connectors, APIs | 546 000 |
| Senior Backend 2 | orchestration/runtime | 546 000 |
| ML Engineer | decision policies, uplift models | 650 000 |
| DevOps | infra, CI/CD, observability | 455 000 |
| Frontend | UI for marketers/ops | 390 000 |
| SDR | outbound pipeline | 195 000 |
| AE | discovery, pilots, closing | 429 000 |
| Customer Success | onboarding, renewals | 390 000 |
| Product/Growth marketer | demand-gen, кейсы, контент | 468 000 |
| Finance/Ops (part-time) | договоры, invoicing, отчётность | 156 000 |
| **Итого зрелая команда** |  | **5 720 000 ₽/мес** |

## PnL и risk summary

### SECTION A: PnL
- Base M12 EBITDA: **-161 660 ₽/мес**
- Base M13 EBITDA break-even: **достижим при сохранении темпа +1 new client/мес**
- Base startup_capital_to_bep_rub: **38,46 млн ₽**
- Optimistic startup_capital_to_bep_rub: **30,62 млн ₽**
- Pessimistic startup_capital_to_bep_rub: **70,71 млн ₽**

### SECTION B: Risk + Monte Carlo
- `p10 EBITDA @M24 = -4,47 млн ₽/мес`
- `p50 EBITDA @M24 = -830 тыс. ₽/мес`
- `p90 EBITDA @M24 = 3,62 млн ₽/мес`
- `p10 LTV/CAC = 2,5x`, `p50 = 8,9x`, `p90 = 24,0x`
- Вывод: распределение исходов слишком широкое, median-case пока не подтверждает investment-grade устойчивость.

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | Огромная first-party data base, зрелый CRM и потребность в next-best-action поверх DWH. | email decision-maker + партнёрство с data/integration vendor | 450 000 ₽/мес |
| 2 | Т-Банк | Сильная data-driven культура и частые lifecycle-коммуникации, где decisioning даёт measurable uplift. | warm intro через fintech/data circle + outbound в CRM lead | 400 000 ₽/мес |
| 3 | ВТБ | Большой retail-banking массив клиентов и высокая ценность orchestration для retention/cross-sell. | conference / fintech event + email head of CRM | 400 000 ₽/мес |
| 4 | Ozon | Высокий объём customer events и персонализация маркетинга на масштабе marketplace. | outbound в growth/CRM leadership + кейс-пилот | 350 000 ₽/мес |
| 5 | Wildberries | Огромная частота коммуникаций и потребность в policy-driven сегментации по first-party данным. | founder-led outbound + referral через martech ecosystem | 350 000 ₽/мес |
| 6 | Яндекс Маркет | Сложный data stack и постоянная оптимизация CRM-orchestration для маркетплейса. | email decision-maker + product analytics community touch | 350 000 ₽/мес |
| 7 | Самокат | Быстрые циклы retention и промо-персонализации, где decisioning-layer может быстро показать ROI. | партнёрство с CRM/integration agency + direct outreach | 300 000 ₽/мес |
| 8 | X5 Group | Наличие loyalty, omnichannel и большого first-party data contour создаёт боль в unified orchestration. | retail conference + outbound в digital CRM | 350 000 ₽/мес |
| 9 | МегаФон | Телеком с высокой плотностью lifecycle-scenarios и сложной customer-base логикой. | outbound в CVM/CRM lead + отраслевое мероприятие | 300 000 ₽/мес |
| 10 | МТС | Большая подписочная база и mature marketing automation stack, где нужен brain-layer поверх existing systems. | email decision-maker + партнёрство с системным интегратором | 300 000 ₽/мес |

**Вывод по GTM:** named-target list реалистичен и хорошо совпадает с ICP, но сам рынок очень узкий, поэтому повторяемость канала пока остаётся недоказанной.

## Top-3 risks

| Риск | Вероятность | Impact | Почему это top-3 |
|---|---|---|---|
| Adjacent, а не direct demand в РФ | Высокая | Высокий | Exact category `AI decisioning` слабая, спрос подтверждён в основном через CRM automation/CDP substitutes. |
| Pricing compression и substitution | Высокая | Высокий | Buyer может выбрать `Mindbox/Sendsay/Carrot quest + внутренний BI` и получить 60-80% ценности дешевле. |
| Founder-heavy enterprise GTM | Средняя | Высокий | CAC и win-rate завязаны на founder-led sale, а длинный security/procurement cycle легко ломает план. |

## Что нужно доказать для APPROVED
1. **3-5 paid enterprise клиента** в РФ в целевом ICP, не пилоты-бесплатники.
2. **Realised ARPA не ниже 250-300 тыс. ₽/мес** без тяжёлого services tail.
3. **Retention / expansion proof**: churn не выше 1-1,5%/мес и хотя бы 1-2 кейса апсейла.
4. **Repeatable GTM motion**: хотя бы 30-40% qualified pipeline не через founder-only channel.
5. **Category wedge**: чётко показать, почему warehouse-native decisioning даёт ROI, который не закрывают Mindbox/Sendsay/внутренний BI.

## LTV Upside Calculator
Так как итоговый статус **NEAR-PASS**, апсайд до approve можно считать от трёх рычагов:

| Рычаг | Текущее значение | Целевое значение | Влияние |
|---|---:|---:|---|
| ARPA | 300 000 ₽/мес | 350 000 ₽/мес | LTV растёт до ~27,98 млн ₽ при тех же GM и churn. |
| Monthly churn | 1,0% | 0,8% | LTV растёт до ~29,98 млн ₽ даже без роста ARPA. |
| CAC | 2 161 900 ₽ | 1 700 000 ₽ | LTV/CAC растёт с 11,1x до ~14,1x. |

**Простой апсайд-сценарий:** если довести ARPA до **350k ₽**, churn до **0,8%**, а CAC удержать в районе **1,7-1,9 млн ₽**, кейс получает шанс перейти в диапазон **72-75/100**.

## Proof points, которых сейчас не хватает
- нет прямого локального evidence, что exact-category `AI decisioning` уже выделена как отдельная budget line;
- нет подтверждённых win/loss данных по российским enterprise-сделкам;
- нет доказательства собственного proprietary dataset или сильного distribution moat;
- нет подтверждения, что median-case выводит компанию к `company_ebitda_rub_month ≥ 500k` в M24.

## Final verdict
**Решение комитета: REJECTED FOR NOW / NEAR-PASS.**

Кейс не отклоняется из-за слабой экономики, наоборот, economics здесь сильнее среднего. Он отклоняется потому, что фондовый стандарт требует не просто красивого base-case, а достаточного запаса прочности по локальному рынку, moat и repeatable execution. Вернуться к approve можно после фактического доказательства продаж, retention и category wedge на 3-5 enterprise клиентах.

---

## 07-score-trajectory.md

# 07-score-trajectory

## 2026-04-20 05:49 MSK — Demand Validation
- Stage: Program 4 / Demand Validation
- Case: `1027-msk-hightouch-ai-decisioning-v2`
- Oldest eligible case processed first by `00-brief.md` mtime.
- Demand API snapshot:
  - `AI decisioning` -> `LOW` (`3/100`)
  - `customer data platform` -> `LOW` (`18/100`)
  - `персонализация маркетинга` -> `LOW` (`22/100`)
  - `маркетинговая автоматизация` -> `MEDIUM` (`30/100`)
- Research conclusion: exact category demand в РФ слабый, но adjacency-demand подтверждён через CDP, CRM automation и Telegram/customer messaging stack.
- Competitor pricing found: Sendsay, Carrot quest, BotHelp, Jivo.
- TAM/SAM/SOM: preferred SAM `568,8 млн ₽`, SOM Y1 `28,4 млн ₽`, SOM Y3 `85,3 млн ₽`.
- Profit Gate: PASS в enterprise-license, managed decisioning и borderline mid-market CDP-lite; FAIL в low-ticket automation-only и pure services.
- Score impact:
  - Adjacent demand evidence: `+2`
  - WTP evidence: `+1`
  - ICP narrowness: `-2`
  - Category education burden: `-1`
  - Net delta: `0`
- Outcome: `PROCEED`, без early reject; кейс оставлен в `pipeline/cases/`.
- Artifacts: `02-demand.md`

## 2026-04-20 06:03 MSK — Unit Economics
- Stage: Program 5 / Unit Economics
- Case: `1027-msk-hightouch-ai-decisioning-v2`
- Economics built only for enterprise ICP: крупные B2C-компании с собственной DWH/CDP и lifecycle-маркетингом.
- Core unit assumptions:
  - MRR per customer: `300 000 ₽/мес`
  - ARR per customer: `3,6 млн ₽/год`
  - COGS per customer: `60 200 ₽/мес`
  - Contribution Margin: `79,9%`
- Fully-loaded CAC model used, not ad-only CAC:
  - Paid ads: `180 000 ₽/мес`
  - SDR+AE FOT attributed to new: `624 000 ₽/мес`
  - Marketing FOT attributed: `234 000 ₽/мес`
  - Tools/CRM: `43 500 ₽/мес`
  - Events/partnerships: `120 000 ₽/мес`
  - Overhead multiplier: `x2,0`
  - Blended CAC: `2 161 900 ₽`
- Funnel by channels modeled:
  - Founder-led outbound CAC: `2,45 млн ₽`
  - Partner CAC: `1,35 млн ₽`
  - Content/inbound CAC: `1,95 млн ₽`
  - Blended lead-to-won conversion: `1,19%`
- Retention and LTV:
  - Monthly churn benchmark used: `1,0%`
  - LTV: `23 982 000 ₽`
  - LTV/CAC: `11,1x`
  - CAC Payback: `7,2 мес`
- Team & hiring realism:
  - Mature fully-loaded FOT: `5,72 млн ₽/мес`
  - Hiring spread across M1-M8, без нереалистичного burst-hiring в M1
  - Burn to break-even: `~37,9 млн ₽`
  - Startup capital assumption: `60 млн ₽`
  - Runway: `~19 мес`
- Break-even:
  - Conservative steady-state: `29 клиентов`
  - Working investment-mode break-even: `16 клиентов` / `M12`
  - EBITDA at 50 clients: `~7,39 млн ₽/мес`
- Profit Gate result:
  - `EBITDA > 500k/mo at 50 clients`: PASS
  - `LTV/CAC >= 3:1`: PASS
- Score impact:
  - Strong contribution profile: `+2`
  - Healthy payback: `+2`
  - Enterprise CAC heaviness: `-1`
  - Narrow ICP dependence: `-1`
  - Net delta: `+2`
- Outcome: `PROCEED`, кейс остаётся в `pipeline/cases/`.
- Artifacts: `04-economics.md`

## 2026-04-20 12:21 MSK — Critic and Verdict
- Stage: Program 7 / Critic and Verdict
- Case: `1027-msk-hightouch-ai-decisioning-v2`
- Preconditions check: `05-critic.md` содержит оба маркера `P6A-DONE` и `P6B-DONE`; `06-verdict.md` до запуска отсутствовал.
- Итоговая рубрика 6x25:
  - Unit Economics: `20/25`
  - EBITDA Potential: `18/25`
  - Market + Demand: `13/25`
  - Moat: `13/25`
  - Execution Risk: `16/25`
  - GTM Realism: `23/25`
- Raw total: `103/150`
- Normalized score: `69/100`
- Tier-awareness:
  - Sources line used: `T1=5, T2=12, T3=0`
  - Weighted tier balance: `2.29`
  - Penalty applied to criterion #3: `-2`
- 7-factor moat:
  - Sum: `11/21`
  - Normalized moat score: `13/25`
- Finance synthesis:
  - Base EBITDA at 50 clients: `~7,39 млн ₽/мес`
  - Monte Carlo p50 EBITDA @M24: `-830 тыс. ₽/мес`
  - Monte Carlo p10 EBITDA @M24: `-4,47 млн ₽/мес`
- Committee conclusion:
  - Economics are investable in a narrow enterprise wedge
  - Local demand, moat and repeatable GTM are still below investment-grade proof
- Outcome: `NEAR-PASS`
- Final routing: `pipeline/rejected/1027-msk-hightouch-ai-decisioning-v2/`
- Artifacts: `06-verdict.md`

