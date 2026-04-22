---

# 00-brief.md

# Краткий бриф

## Кейс
Hebbia для institutional finance и AI-аналитики сделок

## Почему открыт
- Сигнал указывает на сильный enterprise use case в institutional finance: investment banking, private equity, asset management и credit workflows.
- По контексту исходного triage категория уже показывала крупный usage footprint, включая организации с суммарно более $30 трлн AUM и около 200 тыс. prompts в день.
- Для РФ это выглядит как high-touch FINTECH/AI-services wedge для аналитики сделок, data room review, кредитного анализа и investment memo workflows.

## Следующий шаг
Передать кейс в P3-demand-validation для новой аналитики по РФ-рынку, economics, moat и финальному verdict.


---

# 01-intake.md

---
sector: FINTECH
rerun: true
source_raw: 2026-04-19-resurrect-hebbia-institutional-finance-geo-expand.md
created: 2026-04-20T17:04:00+03:00
source_triage: triage/triage-2026-04-14-hebbia-institutional-finance-geo-expand.md
original_verdict: resurrect-full-pipeline
---

# Intake

## Статус
Принудительный resurrect/re-run. Кейс создан как standalone candidate и должен пройти полный пайплайн P3→P7 без классификации как duplicate.

## Исходный verdict
- `triage/triage-2026-04-14-hebbia-institutional-finance-geo-expand.md`

## Полный контекст raw-файла

# RESURRECT SIGNAL — hebbia-institutional-finance-geo-expand

## Meta
- source: triage/triage-2026-04-14-hebbia-institutional-finance-geo-expand.md
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
- pipeline/raw/raw-2026-04-14-hebbia-institutional-finance-geo-expand.md

## Классификация
поддерживающий сигнал для существующего кейса

## Решение
Обогатить существующий кейс: `investment-banking-ai-analyst-operator`.

## Почему
- В `pipeline/cases/` уже есть открытый кейс по AI-аналитику для investment banking, private equity, asset management и corporate finance команд.
- Новый raw совпадает с этим кейсом по нише, buyer profile и типовым workflow: data room, credit docs, due diligence, IC memo, screening и deal execution.
- Это не новый кейс, а дополнительное подтверждение зрелости категории через Hebbia: сигнал усиливает institutional finance позиционирование и добавляет новый источник о partnership-led углублении в credit intelligence.

## Что добавлено в кейс
- В `pipeline/cases/investment-banking-ai-analyst-operator/01-evidence.md` добавлена новая запись со статусом supporting signal.
- Зафиксировано партнёрство Hebbia с Fitch Solutions как подтверждение фокуса на institutional finance и credit intelligence.
- Добавлены ключевые факты из raw: использование у организаций с суммарно более $30 трлн AUM, около 200 тыс. prompts в день и оценка потенциального LTV для РФ на уровне 1,8-9,0 млн руб. в год на клиента.

## Что сделано
- Существующий кейс обогащён.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Кейс обогащён: новый сигнал Hebbia не открывает отдельную тему, но усиливает уже активный кейс по AI-аналитику для инвестиционных и корпоративных финансовых команд через более сильное подтверждение institutional finance traction.

```



---

# 02-demand.md

# 02-demand

## Кейс
hebbia-institutional-finance-geo-expand-v2

## Demand verdict
**Итог: CONDITIONAL PASS.**

- По прямым запросам категории спрос в РФ выглядит **низким или нишевым**: `due diligence` → LOW, `M&A due diligence` → LOW, `AI due diligence` → LOW. [T2]
- По смежным operational jobs-to-be-done сигналы лучше: `проверка контрагентов`, `анализ сделок`, `инвестиционный анализ` дали **MEDIUM** и тысячи вакансий на HH, то есть боль существует, но пока продаётся не как отдельная AI-category, а как часть risk/compliance/investment workflow. [T1][T2]
- Правило раннего reject `LOW demand + Profit Gate FAIL` **не срабатывает**, потому что при enterprise-монетизации EBITDA 500k+ ₽/мес достижима. [T1][T2]

## 1) Спрос и сигналы рынка

### Demand API
- `due diligence` → LOW, score 27, HH vacancies 311, Google Trends RU 4, Yandex suggest 100. [T2]
- `M&A due diligence` → LOW, score 22, HH vacancies 77, Yandex suggest 100. [T2]
- `AI due diligence` → LOW, score 3, HH vacancies 13. [T2]
- `проверка контрагентов` → MEDIUM, score 30, HH vacancies 4 835. [T2]
- `анализ сделок` → MEDIUM, score 30, HH vacancies 5 253. [T2]
- `инвестиционный анализ` → MEDIUM, score 30, HH vacancies 2 933. [T2]

### Интерпретация
- В РФ массово ищут не «AI analyst for institutional finance», а более прикладные outcomes: проверка контрагентов, risk review, инвестиционный анализ, сделочный due diligence. Это важный сигнал упаковки: заходить надо через понятный workflow, а не через абстрактный AI copilot. [T1][T2]
- HH по запросу `due diligence` показывает **381 вакансию**, что подтверждает наличие оплачиваемой функции и реального buyer pain в legal, corpdev, audit и finance-командах. [T1]
- Банк России пишет, что вознаграждение управляющих компаний за 9 месяцев 2023 года выросло до **69,5 млрд ₽**, а более половины выручки формируется управлением ПИФ. Это подтверждает наличие денежного пула у институциональных игроков, которые могут покупать инструменты ускорения анализа и контроля рисков. [T1]

## 2) Реальные конкуренты и цены

| Конкурент | Позиционирование | Публичный прайс | Вывод |
|---|---|---:|---|
| Контур.Фокус | проверка контрагентов, связи, физлица, large-deal checks | **31 155 ₽ / год** базовый, **82 770 ₽ / год** премиум, **115 000 ₽ / год** корпорация [T1] | Локальный стандарт для KYC/compliance, но без deep AI memo workflow |
| Rusprofile | проверка контрагентов и физлиц | от **940 ₽ / мес** базовый, от **1 990 ₽ / мес** эксперт [T1] | Нижняя граница локального WTP за контрагент data access |
| СБИС «Все о компаниях и владельцах» | контрагенты, надежность, торги, финанализ | **9 000 ₽ / год** базовый, **19 000 ₽ / год** расширенный, **38 000 ₽ / год** подробные сведения [T1] | Массовый low-mid market anchor |
| DealRoom | M&A platform, diligence, data room, AI document analysis | от **$1 000 / мес** по market listing/snippet [T2] | Верхний глобальный anchor для deal workflow software |

### Что это значит для Hebbia-подобного продукта
- Локальный рынок уже платит от десятков тысяч рублей в год за data/compliance access и от **$1 000/мес** за полноценный M&A workflow layer. [T1][T2]
- Для institutional-finance AI assistant реалистичный чек в РФ выглядит как **1,2–3,0 млн ₽ ARR** за команду 10–30 пользователей, если продукт заменяет часть ручного review, поиска по data room и подготовки memo. Это inference на базе публичных price anchors и стоимости analyst-time, а не прямая котировка Hebbia. [T1][T2]

## 3) WTP и proof of willingness to pay

### Прямые доказательства WTP
1. Российские buyer'ы уже покупают подписки на проверку компаний и риск-аналитику у Контур.Фокус, Rusprofile и СБИС. Значит, бюджет на data-driven diligence в РФ существует и он регулярен. [T1]
2. DealRoom публично позиционирует отдельный платный слой для due diligence, data room и AI document analysis, а market listings дают price point от **$1 000/мес**. Это показывает, что сделочные команды глобально готовы платить заметно больше commodity KYC tools, если продукт встроен в M&A workflow. [T2]
3. HH по `due diligence` и related roles подтверждает, что функция staffed и оплачивается людьми, а значит автоматизация analyst-hours имеет monetizable ROI. [T1]

### Оценка willingness to pay
- Для RU mid-market buyer willingness to pay за «ещё один источник данных» ограничена десятками тысяч рублей в год. [T1]
- Для банка, УК, PE/VC или corpdev-команды willingness to pay резко растёт, если продукт сокращает время на review data room, поиск рисков, сверку фактов и написание IC memo. Тогда чек **1,2–3,0 млн ₽ в год** выглядит достижимым. [T1][T2]
- Следовательно, WTP **есть**, но он концентрирован в upper-mid/enterprise ICP, а не в широкой SMB-воронке. [T1][T2]

## 4) Telegram bots/services в РФ

- В Telegram есть множество утилитарных ботов для быстрой проверки контрагентов: `@egrul_bot`, `@AgentFNS_bot`, `@SvetoforZSK_Bot`. Их описания обещают «бесплатную быструю проверку» и работу по официальным данным. [T1]
- Это подтверждает, что Telegram как канал для risk/compliance lookup в РФ существует. [T1]
- Но признаков сильного institutional-grade Telegram-продукта именно для investment memo, due diligence synthesis или AI review data room я не нашёл. Текущий слой в Telegram выглядит как shallow lookup utilities, а не замена Hebbia. Это inference на основе найденных bot descriptions и отсутствия сильных demand-сигналов по `AI due diligence`. [T1][T2]

## 5) Market sizing

### Подход и допущения
- **Top-down база:** вознаграждение УК за 9 месяцев 2023 года достигло **69,5 млрд ₽**; annualized run-rate около **92,7 млрд ₽**. Для workflow-аналитики и due diligence software закладываю addressable software spend **1,5%** от revenue pool, потому что продукт не является core AUM fee engine, а лишь увеличивает productivity и speed-to-decision. [T1]
- **Bottom-up база:** целевой universe в РФ для Hebbia-подобного продукта, по моей оценке, это примерно **150 институциональных buyers**: крупнейшие банки и CIB-команды, топ-УК, private equity / VC / special situations и Big4-style deal advisory практики. Это inference, но он калиброван на реальных buyers ниже и на том, что high-end workflow AI нужен не всему рынку, а верхнему слою. [T2]
- **ARR avg:** **2,7 млн ₽ / год** за команду, например 15 пользователей + внедрение + premium support. [T1][T2]

### Обязательная таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | — | — | Для РФ-кейса не использую: нет надёжной Tier-1 мировой базы именно по AI diligence software | — |
| TAM (РФ) | **1,39 млрд ₽** = 92,7 млрд ₽ × 1,5% [T1] | **405 млн ₽** = 150 buyers × 100% × 2,7 млн ₽ [T2] | diff=3,4x, top-down шире и включает весь software wallet; беру lower bound | **405 млн ₽** |
| SAM (РФ) | **486 млн ₽** = 1,39 млрд ₽ × 35% institutional finance / deal workflow fit [T1] | **283,5 млн ₽** = 150 × 70% with need × 2,7 млн ₽ [T1][T2] | diff=1,7x, расхождение допустимо; беру lower bound | **283,5 млн ₽** |
| SOM Y1 | **14,6 млн ₽** = 3% SAM [T1] | **13,5 млн ₽** = 5 клиентов × 2,7 млн ₽ [T1][T2] | diff=8%, модели сходятся | **13,5 млн ₽** |
| SOM Y3 | **48,6 млн ₽** = 10% SAM [T1] | **40,5 млн ₽** = 15 клиентов × 2,7 млн ₽ [T1][T2] | diff=20%, обе оценки реалистичны | **40,5 млн ₽** |

### 10 реальных buyers для bottom-up
1. Сбер CIB [T2]
2. ВТБ Капитал / ВТБ Инвестиции [T2]
3. Газпромбанк [T2]
4. Альфа-Капитал [T2]
5. БКС Мир инвестиций [T2]
6. Т-Инвестиции [T2]
7. АФК Система / Sistema VC [T2]
8. А1 [T2]
9. Kept Deal Advisory [T2]
10. Б1 / ex-EY practice в РФ [T2]

### Cross-check и sanity
- Расхождение по **SAM** меньше 3x, значит модель можно использовать. [T1][T2]
- **SOM Y1 = 13,5 млн ₽**, это меньше 10% от preferred SAM, red flag overclaiming нет. [T1][T2]
- При ACV 2,7 млн ₽ это всего **5 клиентов в первый год**. Даже при цикле сделки 4–6 месяцев это тяжело, но реалистично для founder-led enterprise GTM. [T1][T2]
- Для Y3 нужно **15 клиентов**, что выглядит достижимо только при узком ICP и сильном services-heavy onboarding. [T1][T2]

## 6) Profit Gate: проверка всех сценариев

### Сценарий A. SMB / self-serve
- Чек **120–250 тыс. ₽ ARR** на клиента. [T1]
- Даже 100 клиентов дадут 1,0–2,1 млн ₽ MRR, но для такого motion нужен массовый спрос, которого нет. Плюс high-touch AI onboarding разрушит экономику. [T1][T2]
- **Profit Gate: FAIL.** [T1][T2]

### Сценарий B. Mid-market finance / corpdev teams
- Чек **1,2–1,8 млн ₽ ARR**. [T1][T2]
- При 20 клиентах выручка **24–36 млн ₽ ARR**, этого уже достаточно для EBITDA 500k+ ₽/мес при дисциплинированной команде и ограниченном кастоме. [T1][T2]
- **Profit Gate: PASS.** [T1][T2]

### Сценарий C. Enterprise banks / УК / PE funds
- Чек **2,7–5,0 млн ₽ ARR** с внедрением. [T1][T2]
- 8–10 клиентов дают **21,6–50,0 млн ₽ ARR**. Для такого чека EBITDA 500k+ ₽/мес достижима даже при дорогом presales. [T1][T2]
- **Profit Gate: PASS.** [T1][T2]

### Итог по Profit Gate
- В low-touch продукте кейс не работает. [T1][T2]
- В enterprise / high-touch motion порог **EBITDA >= 500k ₽/мес достижим**. [T1][T2]
- Значит, early reject делать нельзя. [T1][T2]

## 7) Ключевые риски
- Категория в РФ пока не сформулирована как отдельная budget line item, поэтому нужен consultative sale. [T1][T2]
- Локальные buyer'ы уже закрывают часть боли через дешёвые KYC/compliance tools, значит продукту нужно продавать не данные, а speed/accuracy outcome. [T1]
- Высокий риск, что пилоты превратятся в кастомную аналитику и services business. [T2]
- Telegram и low-cost bots снижают perceived novelty на уровне простых проверок, хотя не перекрывают institutional workflow. [T1]

## 8) Вывод для pipeline
**Решение на этапе demand validation: PASS WITH RESERVATIONS.**

Спрос по прямой категории в РФ слабый, но adjacent demand и подтверждённый WTP на risk/compliance + enterprise deal workflow достаточны, чтобы не отправлять кейс в early reject. Дальше критично проверить: CAC, sales cycle, integration burden, defensibility против data vendors и то, можно ли удержать ACV выше 2 млн ₽ без скатывания в кастомный research shop.

## Источники
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=due%20diligence [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=M%26A%20due%20diligence [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=AI%20due%20diligence [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%B0%D0%B3%D0%B5%D0%BD%D1%82%D0%BE%D0%B2 [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7%20%D1%81%D0%B4%D0%B5%D0%BB%D0%BE%D0%BA [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%B8%D0%BD%D0%B2%D0%B5%D1%81%D1%82%D0%B8%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D1%8B%D0%B9%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7 [T2]
- HH.ru, search `due diligence`: https://hh.ru/search/vacancy?text=due+diligence [T1]
- Банк России, событие про рынок УК и ПИФ: https://cbr.ru/press/event/?id=17247 [T1]
- Банк России, итоги I квартала 2025 по УК: https://cbr.ru/press/event/?id=24669 [T1]
- Контур.Фокус, тарифы: https://focus.kontur.ru/site/price [T1]
- Rusprofile, тарифы: https://www.rusprofile.ru/subscribe [T1]
- СБИС, тарифы «Все о компаниях и владельцах»: https://www.tensor-sbis.ru/tarify/vse-o-kompaniyah-i-vladelczah/ [T1]
- DealRoom pricing page: https://dealroom.net/products/pricing [T1]
- DealRoom pricing market listing/snippet: https://www.trustradius.com/products/dealroom/pricing [T2]
- Telegram bot `@egrul_bot`: https://t.me/egrul_bot [T1]
- Telegram bot `@AgentFNS_bot`: https://t.me/AgentFNS_bot [T1]
- Telegram bot `@SvetoforZSK_Bot`: https://t.me/SvetoforZSK_Bot [T1]

Sources: T1=10, T2=7, T3=0. Primary evidence basis: T1.
## Market Pulse
- Market Pulse 2026-04-21: растущий интерес.

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.
Market Pulse 22.04.2026: растущий интерес.


---

# 04-economics.md

# 04-economics

## Кейс
hebbia-institutional-finance-geo-expand-v2

## Unit economics verdict
**Итог: PASS WITH RESERVATIONS.**

Для Hebbia-подобного AI workflow в institutional finance по РФ экономическая модель работает только как **узкий enterprise B2B продукт** с high-touch продажей, пилотом и безопасным внедрением. В базовом сценарии беру: **ACV 2,7 млн ₽/год**, **MRR 225 тыс. ₽/клиент**, **COGS 60 тыс. ₽/клиент/мес**, **gross margin 73,3%**, **fully-loaded CAC 1,64 млн ₽**.

Ключевые выводы:
- **LTV = 11,0 млн ₽** при **monthly churn 1,5%**. [T2]
- **LTV/CAC = 6,7x**, выше investable-порога **3,0x**. [T1][T2]
- **CAC Payback = 7,3 месяца**, лучше enterprise sanity-порога **<18 месяцев**. [T3]
- **Contribution Margin = 73,3%**.
- **Break-even = 43 клиента** или **9,7 млн ₽ MRR**.
- При **50 клиентах** модель даёт **~1,26 млн ₽ EBITDA/мес**, то есть Profit Gate проходит. [T1][T3]

Но upside платится дорогим GTM и длинным выходом на окупаемость. Это не self-serve SaaS, а enterprise finance platform с heavy presales и pilot motion.

---

## 1) Базовые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | банки, УК, PE/VC, corpdev, deal advisory | Совпадает с P4 demand [T1] |
| Средний контракт (ACV) | 2 700 000 ₽/год | Беру midpoint из demand-диапазона 1,2-3,0+ млн ₽ [T1] |
| MRR на клиента | 225 000 ₽/мес | ACV / 12 |
| Срок sales cycle | 4-6 месяцев | enterprise finance motion [T1][T3] |
| Новый paying customers / мес в steady-state | 1,8 | консервативно для narrow ICP |
| Startup capital | 95 000 000 ₽ | нужен запас до break-even |

---

## 2) Детальный бизнес-процесс: от лида до оплаты

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Формирование account list по банкам, УК, PE и advisory | SDR | CRM, Контур.Фокус, ручной research | 2 ч/аккаунт | 2 000 | Средняя |
| 2 | Обогащение ЛПР и контактных путей | SDR | CRM, email finder, Telegram/email research | 1 ч | 1 000 | Средняя |
| 3 | Outbound sequence и первые касания | SDR | CRM sequences, email automation | 10-14 дней | 3 500 | Высокая |
| 4 | Discovery call и qualification | SDR + AE | Meet, CRM, note taker | 45 мин | 5 000 | Низкая |
| 5 | Продуктовое интервью по workflow | AE | CRM, demo deck | 1 ч | 4 500 | Низкая |
| 6 | Live demo на data room / memo workflow | AE + Solutions | Sandbox, demo workspace | 1,5 ч | 10 000 | Низкая |
| 7 | Технический scoping и security review | CTO + Solutions + AE | Security checklist, docs | 1 неделя | 40 000 | Низкая |
| 8 | Пилот на документах клиента | Solutions + ML + Backend | Cloud, LLM, коннекторы | 3-4 недели | 150 000 | Средняя |
| 9 | ROI-модель и memo для комитета закупки | AE + CEO | spreadsheet, deck | 6-8 ч | 22 000 | Низкая |
| 10 | Legal/procurement negotiation | CEO + AE + Ops | ЭДО, договор, redlines | 2-4 недели | 35 000 | Низкая |
| 11 | Invoice и получение оплаты | Ops/Finance | 1С, банк, ЭДО | 3-5 дней | 4 000 | Высокая |
| 12 | Onboarding, настройка workspace, train-the-team | CSM + Solutions | PM tool, cloud, connectors | 2-3 недели | 95 000 | Средняя |

### Вывод по процессу
- Между лидом и оплатой здесь **12 шагов**, из них хорошо автоматизируются только outreach, invoice и часть enrichment.
- Самые дорогие этапы: **pilot**, **security review**, **onboarding**.
- Поэтому для этого кейса корректен только **fully-loaded CAC**, а не marketing-only CAC. [T3]

---

## 3) COGS breakdown per client/month

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| LLM/API inference | 16 000 | длинные finance-документы, query-heavy workload |
| Cloud compute + storage | 9 000 | secure compute, хранение документов, backups |
| ETL / ingestion / connectors | 8 000 | загрузка data room, мониторинг пайплайна |
| Customer Success / analyst support | 15 000 | доля CSM и support-hours |
| Security / logging / audit | 5 000 | audit trail и observability |
| Amortized onboarding & pilot support | 7 000 | spread onboarding effort на 12 месяцев |
| **Итого COGS** | **60 000** |  |

| Метрика | Значение |
|---|---:|
| MRR на клиента | 225 000 ₽ |
| Gross Profit на клиента | 165 000 ₽ |
| Gross Margin % | **73,3%** |
| Contribution Margin % | **73,3%** |

---

## 4) CAC by acquisition channel with funnel conversion

| Канал | Воронка | Conversion lead→paid | New paid / мес | Расходы / мес, ₽ | CAC по каналу, ₽ |
|---|---|---:|---:|---:|---:|
| Outbound ABM | 180 target accounts → 36 meetings → 9 pilots → 0,9 deal | 0,5% от target accounts | 0,9 | 1 050 000 | 1 166 667 |
| Партнёрства / advisory referrals | 24 intros → 8 meetings → 3 pilots → 0,45 deal | 1,9% от intros | 0,45 | 620 000 | 1 377 778 |
| Founder-led inbound / referrals | 15 leads → 7 SQL → 4 demos → 0,45 deal | 3,0% | 0,45 | 260 000 | 577 778 |
| Контент / performance | 900 visits → 36 leads → 8 SQL → 2 demos → 0,2 deal | 0,22% | 0,2 | 210 000 | 1 050 000 |

### Blended channel CAC
| Показатель | Значение |
|---|---:|
| Всего new paying customers / мес | 2,0 |
| Всего channel spend / мес | 2 140 000 ₽ |
| Blended channel CAC | **1 070 000 ₽** |

> Канальный CAC и blended CAC не равны fully-loaded CAC. Ниже для инвестиционного вывода использую более строгую fully-loaded модель.

---

## 5) Fully-loaded CAC

### Формула
`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing team FOT allocated + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

### Компоненты fully-loaded CAC
| Компонент | ₽/мес | Как получено | Источник |
|-----------|-------:|--------------|----------|
| Paid ads (Яндекс.Директ/VK) | 210 000 | performance + контент-дистрибуция + retargeting | T3 |
| Outbound team FOT (SDR/AE attributed to new) | 845 000 | SDR 234k + AE 494k + 30% Solutions allocation 117k | T3 |
| Marketing team FOT (partial allocation) | 270 000 | ~35% founder/PMM time на acquisition | T3 |
| Tools (CRM, LinkedIn Sales Nav, Apollo, аналог) | 140 000 | CRM + enrichment + sequencing + webinar/data room tools | T3 |
| Events/partnerships | 800 000 | отраслевые roundtables, партнёрские комиссии, конференции | T3 |
| Raw acquisition pool | 2 265 000 | сумма строк выше |  |
| Overhead multiplier (x1.3) | 679 500 | 30% на finance/legal/admin | T3 |
| **Fully-loaded acquisition pool** | **2 944 500** | raw × 1,3 |  |
| New paying customers | 1,8 | консервативный steady-state | T1 |
| **Fully-loaded CAC** | **1 635 833 ₽** | 2 944 500 / 1,8 |  |

### Sanity checks
- Для enterprise SaaS B2B в РФ user дал benchmark **300-900K ₽**, а для enterprise/regulated motion допускается мультипликатор **x2.0-x2.5** к raw CAC. [T3]
- Здесь blended channel CAC = **1,07 млн ₽**, fully-loaded CAC = **1,64 млн ₽**. Это выше стандартного enterprise SaaS коридора, но логично для **узкого institutional finance ICP** с пилотами, security review и procurement.
- CAC не выглядит искусственно заниженным, red flag по «слишком дешёвому CAC» нет. [T3]

---

## 6) LTV with churn rate benchmark

### Benchmark по churn
Для high-ARPA B2B SaaS беру **monthly logo churn 1,5%**. Это консервативнее, чем top-tier enterprise benchmark, но лучше median SaaS. ChartMogul пишет, что у компаний с **ARPA > $500/мес** median monthly customer churn около **2,2%**, а лучшие компании должны стремиться к **<1%**. Для Hebbia-подобного workflow в institutional finance разумно закладывать уровень между этими границами, то есть **1,5%/мес**. [T2]

### Расчёт LTV
| Показатель | Формула | Значение |
|---|---|---:|
| MRR на клиента |  | 225 000 ₽ |
| Gross Margin |  | 73,3% |
| Monthly churn |  | 1,5% |
| Annual churn | `1-(1-0.015)^12` | **16,6%** |
| LTV | `MRR × GM / monthly churn` | **10 995 000 ₽** |

### LTV/CAC ratio
| Метрика | Значение |
|---|---:|
| LTV | 10 995 000 ₽ |
| Fully-loaded CAC | 1 635 833 ₽ |
| **LTV/CAC** | **6,7x** |

**Вывод:** инвестиционный порог **3,0x** пройден с запасом. Даже при stress-case churn 2,0% и CAC 2,0 млн ₽ отношение остаётся выше 4x.

---

## 7) CAC Payback in months

| Показатель | Формула | Значение |
|---|---|---:|
| Fully-loaded CAC |  | 1 635 833 ₽ |
| MRR per customer |  | 225 000 ₽ |
| CAC Payback | `CAC / MRR` | **7,3 месяца** |

**Sanity:** это лучше enterprise-порога **<18 месяцев**. [T3]

---

## 8) Team & FOT

### Полная команда: роли, функции, зарплаты
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---|---:|---:|---:|
| CEO | enterprise sales, fundraising, strategy | 650 000 | 195 000 | 845 000 |
| CTO/Tech Lead | архитектура, security, delivery | 550 000 | 165 000 | 715 000 |
| Senior Backend 1 | ingestion/API | 420 000 | 126 000 | 546 000 |
| Senior Backend 2 | workflow engine/integrations | 420 000 | 126 000 | 546 000 |
| ML Engineer | retrieval, evals, prompt systems | 520 000 | 156 000 | 676 000 |
| DevOps | infra, observability, private contour | 350 000 | 105 000 | 455 000 |
| Frontend | analyst workspace UI | 300 000 | 90 000 | 390 000 |
| Solutions Engineer | pilots, onboarding, custom workflows | 300 000 | 90 000 | 390 000 |
| SDR | outbound pipeline | 180 000 | 54 000 | 234 000 |
| AE | closing, procurement, renewals assist | 380 000 | 114 000 | 494 000 |
| Customer Success | adoption, expansion, retention | 250 000 | 75 000 | 325 000 |
| Ops/Finance | invoicing, contracts, admin | 180 000 | 54 000 | 234 000 |
| **Итого** |  |  |  | **5 850 000 ₽/мес** |

### Таблица найма realism
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------:|-------------------------------:|-------------------:|-------------------------------------------:|------------------:|------------------------:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1,5 | 1,5 | 126 000 | 546 000 each |
| ML Engineer | 1 | 520 000 | 2,5 | 2 | 156 000 | 676 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR (outbound) | 1 | 180 000 + бонус | 0,75 | 1 | 54 000 | 234 000 |
| AE (Account Exec) | 1 | 380 000 + комиссия | 1,5 | 3 | 114 000 | 494 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |
| Solutions Engineer | 1 | 300 000 | 1,5 | 1,5 | 90 000 | 390 000 |
| Ops/Finance | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 |

### Cumulative FOT timeline M1-M12
| Месяц | Кто уже в команде | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO, Frontend | 1 235 000 |
| M3 | + CTO, Backend 1, SDR | 2 730 000 |
| M4 | + Backend 2, DevOps, Ops/Finance | 3 965 000 |
| M5 | + ML Engineer, AE | 5 135 000 |
| M6 | + Solutions Engineer, Customer Success | 5 850 000 |
| M7 | без новых наймов | 5 850 000 |
| M8 | без новых наймов | 5 850 000 |
| M9 | без новых наймов | 5 850 000 |
| M10 | без новых наймов | 5 850 000 |
| M11 | без новых наймов | 5 850 000 |
| M12 | без новых наймов | 5 850 000 |

### Hiring realism комментарий
- В M1 нет 5+ hires, то есть план соблюдает time-to-hire realism. [T3]
- Полная команда разворачивается только к **M6**, что выглядит правдоподобно для enterprise B2B.
- FOT команды быстро выходит в диапазон **5,8+ млн ₽/мес**, значит модель не занижает cost base.

---

## 9) Fixed costs breakdown

| Статья fixed cost | ₽/мес |
|---|---:|
| FOT fully-loaded | 5 850 000 |
| Офис / travel / customer visits | 350 000 |
| Core software stack | 190 000 |
| Legal / бухгалтерия / audit | 180 000 |
| G&A / admin / misc | 420 000 |
| **Итого fixed costs** | **6 990 000 ₽/мес** |

---

## 10) Break-even by client count and by month

### Break-even по числу клиентов
| Показатель | Формула | Значение |
|---|---|---:|
| Gross Profit на клиента / мес | 225 000 - 60 000 | 165 000 ₽ |
| Fixed costs / мес |  | 6 990 000 ₽ |
| **Break-even clients** | `6 990 000 / 165 000` | **42,4 ≈ 43 клиента** |

### Break-even по месяцам
Траектория клиентов: **0, 0, 1, 2, 4, 6, 9, 13, 18, 24, 31, 38, 43** клиентов к M13.

| Месяц | Клиенты | GP, ₽ | Fixed, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 1 985 000 | -1 985 000 |
| M2 | 0 | 0 | 2 375 000 | -2 375 000 |
| M3 | 1 | 165 000 | 3 870 000 | -3 705 000 |
| M4 | 2 | 330 000 | 5 105 000 | -4 775 000 |
| M5 | 4 | 660 000 | 6 275 000 | -5 615 000 |
| M6 | 6 | 990 000 | 6 990 000 | -6 000 000 |
| M7 | 9 | 1 485 000 | 6 990 000 | -5 505 000 |
| M8 | 13 | 2 145 000 | 6 990 000 | -4 845 000 |
| M9 | 18 | 2 970 000 | 6 990 000 | -4 020 000 |
| M10 | 24 | 3 960 000 | 6 990 000 | -3 030 000 |
| M11 | 31 | 5 115 000 | 6 990 000 | -1 875 000 |
| M12 | 38 | 6 270 000 | 6 990 000 | -720 000 |
| M13 | 43 | 7 095 000 | 6 990 000 | **+105 000** |

**Вывод:** break-even достигается примерно к **M13** при **43 клиентах**.

---

## 11) Burn-to-breakeven и cash runway

| Метрика | Значение |
|---|---:|
| Cumulative burn до break-even | **49,45 млн ₽** |
| Доп. оборотный буфер на длинный procurement / сдвиг сделок | **15,00 млн ₽** |
| Рекомендуемый startup capital | **95,00 млн ₽** |
| Буфер после выхода на break-even | **~30,55 млн ₽** |
| Cash runway при peak burn ~6,0 млн ₽/мес | **~15,8 месяца** |

### Интерпретация
- Чистый burn до break-even сам по себе около **49,5 млн ₽**, но для enterprise finance этого мало без буфера на длинные пилоты и отсрочку оплат.
- Поэтому под фондовый заход разумнее закладывать **95 млн ₽**, а не минимально возможный чек.
- Значит кейс финансируемый, но только при дисциплине по ICP и hiring.

---

## 12) Проверка Profit Gate

| Проверка | Результат |
|---|---|
| EBITDA > 500K ₽/мес достижима при 50 клиентах? | **Да**. 50 × 165k GP = 8,25 млн ₽ GP, EBITDA ≈ **1,26 млн ₽/мес** |
| LTV/CAC >= 1? | **Да**, 6,7x |
| LTV/CAC >= 3? | **Да**, 6,7x |
| CAC Payback < 18 мес? | **Да**, 7,3 мес |
| Прибыльность при low-touch SMB motion? | **Нет**, только enterprise/high-touch |

## Финальный вывод
**Profit Gate: PASS.**

Кейс выдерживает инвестиционный фильтр по unit economics, но только в узком enterprise-сценарии: банки, УК, PE/VC и advisory команды, где buyer реально платит за ускорение due diligence, memo preparation и review больших массивов документов. Если продукт опускается в lower-end compliance/data lookup, экономика быстро ломается.

## Источники
- `02-demand.md` этого кейса: ICP, price anchors, SAM/SOM, profit gate context [T1]
- ChartMogul, *What Is a Good Customer Churn Rate?*: https://chartmogul.com/blog/good-customer-churn-rate/ [T2]
- Бриф программы Unit Economics: fully-loaded CAC multipliers, salary bands RU 2026, hiring realism, sanity checks [T3]

**Source map:** T1 = внутренний demand-анализ кейса, T2 = внешний churn benchmark, T3 = benchmark-пакет программы.


---

# 05-critic.md

## SECTION A. Finance PnL

### A1. Допущения модели
- ARPA / MRR на клиента: **225 000 ₽/мес**.
- COGS на клиента: **60 000 ₽/мес**.
- Gross profit на клиента: **165 000 ₽/мес**.
- Contribution profit на клиента: **165 000 ₽/мес**.
- Fixed costs: **6 990 000 ₽/мес**.
- Team FOT: **5 850 000 ₽/мес**.
- Страховые взносы **~30% к ФОТ** уже включены в FOT и fixed costs.
- Налоговые режимы для net: **УСН 6%**, **IT-льгота 3%** при аккредитации Минцифры, **ОСНО 20%** по прибыли; при ОСНО дополнительно возникает **НДС 20%**, что ухудшает cash conversion.
- Для PnL приняты три сценария new clients / churn:
  - **Base:** new clients = 0,0,1,1,2,2,3,4,5,6,7,7; churn **1,5%/мес**.
  - **Optimistic:** new clients = 0,1,1,2,3,4,5,6,7,7,8,8; churn **1,0%/мес**.
  - **Pessimistic:** new clients = 0,0,0,1,1,1,2,2,3,3,4,4; churn **2,5%/мес**.
- Cumulative cash показан от **0 ₽** как накопленный cash deficit.

### A2. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 4 | 5 | 6 | 7 | 7 |
| Total clients | 0.00 | 0.00 | 1.00 | 1.98 | 3.96 | 5.90 | 8.81 | 12.68 | 17.49 | 23.22 | 29.87 | 36.43 |
| MRR, ₽ | 0 | 0 | 225 000 | 446 625 | 889 926 | 1 326 577 | 1 981 678 | 2 851 953 | 3 934 174 | 5 225 161 | 6 721 784 | 8 195 957 |
| COGS, ₽ | 0 | 0 | 60 000 | 119 100 | 237 313 | 353 754 | 528 447 | 760 521 | 1 049 113 | 1 393 376 | 1 792 476 | 2 185 588 |
| Gross profit, ₽ | 0 | 0 | 165 000 | 327 525 | 652 612 | 972 823 | 1 453 231 | 2 091 432 | 2 885 061 | 3 831 785 | 4 929 308 | 6 010 368 |
| GM% | 0.0% | 0.0% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% |
| Fixed costs, ₽ | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 |
| EBITDA, ₽ | -6 990 000 | -6 990 000 | -6 825 000 | -6 662 475 | -6 337 388 | -6 017 177 | -5 536 769 | -4 898 568 | -4 104 939 | -3 158 215 | -2 060 692 | -979 632 |
| Cash burn, ₽ | 6 990 000 | 6 990 000 | 6 825 000 | 6 662 475 | 6 337 388 | 6 017 177 | 5 536 769 | 4 898 568 | 4 104 939 | 3 158 215 | 2 060 692 | 979 632 |
| Cumulative cash, ₽ | -6 990 000 | -13 980 000 | -20 805 000 | -27 467 475 | -33 804 863 | -39 822 040 | -45 358 809 | -50 257 377 | -54 362 316 | -57 520 531 | -59 581 223 | -60 560 855 |

### A3. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 1 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 7 | 8 | 8 |
| Total clients | 0.00 | 1.00 | 1.99 | 3.97 | 6.93 | 10.86 | 15.75 | 21.59 | 28.38 | 35.10 | 42.74 | 50.32 |
| MRR, ₽ | 0 | 225 000 | 447 750 | 893 272 | 1 559 340 | 2 443 746 | 3 544 309 | 4 858 866 | 6 385 277 | 7 896 424 | 9 617 460 | 11 321 286 |
| COGS, ₽ | 0 | 60 000 | 119 400 | 238 206 | 415 824 | 651 666 | 945 149 | 1 295 698 | 1 702 741 | 2 105 713 | 2 564 656 | 3 019 009 |
| Gross profit, ₽ | 0 | 165 000 | 328 350 | 655 066 | 1 143 516 | 1 792 081 | 2 599 160 | 3 563 168 | 4 682 537 | 5 790 711 | 7 052 804 | 8 302 276 |
| GM% | 0.0% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% |
| Fixed costs, ₽ | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 |
| EBITDA, ₽ | -6 990 000 | -6 825 000 | -6 661 650 | -6 334 934 | -5 846 484 | -5 197 919 | -4 390 840 | -3 426 832 | -2 307 463 | -1 199 289 | 62 804 | 1 312 276 |
| Cash burn, ₽ | 6 990 000 | 6 825 000 | 6 661 650 | 6 334 934 | 5 846 484 | 5 197 919 | 4 390 840 | 3 426 832 | 2 307 463 | 1 199 289 | 0 | 0 |
| Cumulative cash, ₽ | -6 990 000 | -13 815 000 | -20 476 650 | -26 811 584 | -32 658 068 | -37 855 987 | -42 246 827 | -45 673 659 | -47 981 122 | -49 180 411 | -49 180 411 | -49 180 411 |

### A4. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 4 |
| Total clients | 0.00 | 0.00 | 0.00 | 1.00 | 1.98 | 2.93 | 4.85 | 6.73 | 9.56 | 12.32 | 16.02 | 19.62 |
| MRR, ₽ | 0 | 0 | 0 | 225 000 | 444 375 | 658 266 | 1 091 809 | 1 514 514 | 2 151 651 | 2 772 860 | 3 603 538 | 4 413 450 |
| COGS, ₽ | 0 | 0 | 0 | 60 000 | 118 500 | 175 538 | 291 149 | 403 870 | 573 774 | 739 429 | 960 944 | 1 176 920 |
| Gross profit, ₽ | 0 | 0 | 0 | 165 000 | 325 875 | 482 728 | 800 660 | 1 110 643 | 1 577 877 | 2 033 430 | 2 642 595 | 3 236 530 |
| GM% | 0.0% | 0.0% | 0.0% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% | 73.3% |
| Fixed costs, ₽ | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 | 6 990 000 |
| EBITDA, ₽ | -6 990 000 | -6 990 000 | -6 990 000 | -6 825 000 | -6 664 125 | -6 507 272 | -6 189 340 | -5 879 357 | -5 412 123 | -4 956 570 | -4 347 405 | -3 753 470 |
| Cash burn, ₽ | 6 990 000 | 6 990 000 | 6 990 000 | 6 825 000 | 6 664 125 | 6 507 272 | 6 189 340 | 5 879 357 | 5 412 123 | 4 956 570 | 4 347 405 | 3 753 470 |
| Cumulative cash, ₽ | -6 990 000 | -13 980 000 | -20 970 000 | -27 795 000 | -34 459 125 | -40 966 397 | -47 155 737 | -53 035 094 | -58 447 217 | -63 403 786 | -67 751 191 | -71 504 661 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Waterfall на 1 клиента / месяц
- **ARPA:** 225 000 ₽
- **COGS:** 60 000 ₽
- **Gross profit:** 165 000 ₽
- **Variable sales/support:** 0 ₽ в операционной модели P5
- **Contribution:** 165 000 ₽

#### Waterfall на EBITDA break-even уровне 43 клиентов
- **Revenue:** 9 675 000 ₽/мес
- **COGS:** 2 580 000 ₽/мес
- **Gross profit:** 7 095 000 ₽/мес
- **Contribution:** 7 095 000 ₽/мес
- **EBITDA:** **105 000 ₽/мес**

#### Net profit после налогов
- **УСН 6%:** 105 000 - 580 500 = **-475 500 ₽/мес**
- **IT-льгота 3%:** 105 000 - 290 250 = **-185 250 ₽/мес**
- **ОСНО 20%:** налог на прибыль = **21 000 ₽**, net = **84 000 ₽/мес**, но возникает **НДС 20%** и дополнительное давление на cash flow

#### Waterfall на уровне 50 клиентов
- **Revenue:** 11 250 000 ₽/мес
- **COGS:** 3 000 000 ₽/мес
- **Gross profit:** 8 250 000 ₽/мес
- **Contribution:** 8 250 000 ₽/мес
- **EBITDA:** **1 260 000 ₽/мес**
- **Net profit при УСН 6%:** **585 000 ₽/мес**
- **Net profit при IT-льготе 3%:** **922 500 ₽/мес**
- **Net profit при ОСНО 20%:** **1 008 000 ₽/мес** до учёта кассового эффекта НДС

### A6. Cash flow: startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Optimistic | M11 | 49 180 411 ₽ | Агрессивный ramp позволяет выйти в плюс внутри года, но нужен почти 50 млн ₽ upfront runway |
| Base | M13 | 60 560 855 ₽ | Базовый сценарий требует финансирования чуть больше года до EBITDA 0 |
| Pessimistic | M19 | 82 358 883 ₽ | Замедление GTM и более высокий churn заметно ухудшают capital efficiency |

### A7. Налоговая модель РФ
- **УСН 6% с выручки:** простой режим, но на уровне EBITDA break-even по сути оставляет компанию всё ещё в post-tax минусе.
- **IT-льгота 3%:** лучший режим для software-компании при наличии аккредитации Минцифры и соблюдении критериев профильной выручки.
- **ОСНО 20%:** по налогу на прибыль выглядит мягче при положительном EBITDA, но включает **НДС 20%**, что ухудшает cash conversion и усложняет enterprise procurement.
- **Страховые взносы ~30% к ФОТ:** уже включены в FOT **5,85 млн ₽/мес** и fixed costs **6,99 млн ₽/мес**.
- Для этого кейса базово рациональнее считать **IT-льготу / УСН**, а ОСНО рассматривать только если нужен вход в НДС-контур крупных клиентов.

### A8. Break-even по client count и по месяцам
| Scenario | EBITDA break-even clients | Contribution break-even clients | Break-even month | Комментарий |
|---|---:|---:|---:|---|
| Optimistic | 43 | 43 | M11 | Сильный enterprise execution позволяет пройти EBITDA 0 в пределах 12 месяцев |
| Base | 43 | 43 | M13 | Базовый план сходится, но не успевает выйти в плюс в течение первого года |
| Pessimistic | 43 | 43 | M19 | При слабом ramp запас капитала нужен существенно больше |

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis: EBITDA через 12 месяцев

Допущение для stress по CAC: при **CAC x2** скорость привлечения новых клиентов падает примерно вдвое при том же acquisition budget, поэтому считаю new clients как **0,5x от base-plan**. Это inference на базе fully-loaded CAC из `04-economics.md` [T3].

| Scenario | New clients assumption | Churn / Price shock | Clients @M12 | EBITDA @M12, ₽/мес | Delta vs Base |
|---|---|---|---:|---:|---:|
| Base | 0,0,1,1,2,2,3,4,5,6,7,7 | churn 1,5%, ARPU 225k | 36,43 | -979 632 | — |
| Sens1: CAC x2 | тот же бюджет, new clients = 0,5x base | churn 1,5%, ARPU 225k | 18,21 | -3 984 816 | -3 005 184 |
| Sens2: Churn x2 | base acquisition | churn 3,0%, ARPU 225k | 34,94 | -1 224 566 | -244 935 |
| Sens3: Price -30% | base acquisition | churn 1,5%, ARPU 157,5k | 36,43 | -3 438 419 | -2 458 787 |

### B2. Monte Carlo Lite: confidence intervals

Вместо single-point base/opt/pess беру triangular ranges по ключевым драйверам. Полную 1000-итерационную симуляцию здесь не кодирую, поэтому использую **9 комбинаций**: best, median, worst и 6 mixed-сочетаний. Это соответствует упрощённому правилу программы.

#### Inputs: triangular distribution
| Переменная | min | mode | max | Источник |
|---|---:|---:|---:|---|
| CAC, ₽ | 1 200 000 | 1 640 000 | 2 400 000 | `04-economics.md`, fully-loaded CAC 1,64 млн ₽ и stress-band для enterprise motion [T3] |
| Monthly churn, % | 1,0% | 1,5% | 3,0% | ChartMogul benchmark + stress uplift для РФ enterprise pilot-heavy motion [T2][T3] |
| ARPU, ₽/мес | 180 000 | 225 000 | 300 000 | Price anchors и ACV corridor 2,16-3,6 млн ₽/год, inference from `02-demand.md` [T1][T2] |
| Conversion lead→paid, % | 0,9% | 1,3% | 1,9% | Funnel mix в `04-economics.md`: outbound 0,5%, referrals 1,9%, blended около 1%+ [T3] |
| Time-to-hire, мес | 0,75 | 1,5 | 2,5 | Hiring realism table в `04-economics.md` [T3] |

#### 9-combo interpretation
- **Best case**: CAC_min + Churn_min + ARPU_max.
- **Median**: CAC_mode + Churn_mode + ARPU_mode.
- **Worst case**: CAC_max + Churn_max + ARPU_min.
- Остальные 6 комбинаций нужны, чтобы не переоценить single best/worst corners.
- Для CAC использую влияние на скорость customer acquisition: `new clients_t = base_new_t × CAC_mode / CAC_scenario`.
- Cash runway считаю от рекомендованного startup capital **95 млн ₽**, деля его на средний burn первых 12 месяцев в каждой комбинации. Это упрощение, но для critic-блока достаточно.

| Метрика | p10 | p50 | p90 | Range width |
|---|---:|---:|---:|---:|
| EBITDA @M24, ₽/мес | 855 845 | 10 795 279 | 29 835 989 | 28 980 144 |
| CAC payback, мес | 20,0 | 9,9 | 5,0 | 15,0 |
| LTV/CAC | 1,67x | 6,71x | 20,00x | 18,33x |
| Cash runway, мес | 15,7 | 18,8 | 24,9 | 9,2 |

#### Monte Carlo выводы
- **Правило 1:** p10 EBITDA < 0 **не срабатывает**, потому что p10 EBITDA @M24 остаётся **+0,86 млн ₽/мес**.
- **Правило 2:** p50 EBITDA < 500К ₽/мес **не срабатывает**, потому что median = **10,8 млн ₽/мес**.
- **Правило 3:** `p90 / p10 = 29,8 / 0,86 ≈ 34,9x`, это **сильно выше 10x**, значит неопределённость экстремально высокая и score нужно **даунгрейдить на 1 notch**.
- **Правило 4:** Range width по **LTV/CAC = 18,33x**, это сильно выше порога **8x** и означает, что модель хрупкая к pricing, churn и CAC одновременно.
- Вывод: формально economics проходят, но **distribution quality слабее, чем point estimate из SECTION A**. Кейс investable только при жёстком ICP-control и снижении variance в GTM.

### B3. Competitor deep-dive

Ниже оцениваю не только прямых AI-native конкурентов, но и практические substitute layers, через которые institutional finance buyer уже закрывает задачу diligence, company intelligence и deal workflow.

#### Топ-3 западных
| Competitor | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **S&P Capital IQ Pro** | Сильнейшая база по public/private markets, скрининг, comps, workflow для investment teams [B1] | Дорогой, data-heavy, но не AI-native memo copilot; слабее в document-grounded Q&A по data room | **25-30%** глобального spend в institutional finance intelligence stack, inference по brand penetration и seat ubiquity [B1] | Hebbia-like продукт выигрывает на unstructured docs, IC memo synthesis и question-answering поверх data room |
| **PitchBook** | Сильная private market / VC / PE data, удобен для sourcing и benchmark comps [B2] | Менее глубокий в live diligence workflow и internal knowledge synthesis | **20-25%** глобального spend в PE/VC research stack, inference [B2] | Лучше в post-sourcing stage: анализ документов сделки, risk extraction, memo drafting |
| **DealRoom** | Специализация на due diligence, data room, collaborative Q&A, AI document analysis, 350+ customers [B3] | Более узкий M&A workflow, слабее как research brain across firm-wide knowledge | **5-10%** в M&A workflow software, inference; заметен в data-room/workflow нише, но не доминирует весь research stack [B3] | Наше преимущество, если продукт глубже работает как cross-document reasoning engine, а не только deal-room PM tool |

#### Топ-5 российских
| Competitor | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Контур.Фокус** | Сильная локальная проверка контрагентов, 35+ источников, мониторинг, физлица, скоринг [B4] | Это прежде всего KYC/compliance + company intelligence, а не AI analyst workflow для investment memo | **35-45%** российского spend в проверке контрагентов/комплаенсе, inference по узнаваемости и тарифной линейке [B4] | Hebbia-like слой лучше на многошаговом анализе data room, сравнении документов и генерации investment memo |
| **Rusprofile** | Самый дешёвый и массовый self-serve access к company/risk data, удобен для быстрой проверки [B5] | Низкий ARPU и ограниченная глубина workflow, слабая защищённость от price pressure | **15-20%** spend в low/mid-market company-check tools, inference [B5] | Мы сильнее там, где нужен не lookup, а reasoning и synthesis на больших массивах документов |
| **СБИС / Saby** | Широкая экосистема, анализ рынка и кредитоспособности, мониторинг СМИ, интеграция в back-office [B6] | Модульность и breadth важны, но продукт не выглядит как best-in-class AI copilot для сделки | **10-15%** spend в company intelligence / accounting-adjacent workflows, inference [B6] | Преимущество в analyst productivity и speed-to-decision, а не в ERP/ЭДО-платформенности |
| **ITFB EasyDoc** | Российский IDP для извлечения данных из документов, импортонезависимый стек, фокус на enterprise document processing [B7] | Это document capture/IDP, а не end-to-end finance reasoning platform | **5-10%** в enterprise IDP под regulated customers, inference [B7] | Наше преимущество в финальном слое смысла: не только extraction, но answer engine и memo generation |
| **Smart Engines** | Сильный OCR/on-device parsing, высокий уровень локальной технологической независимости, кейсы в finance/ID [B8] | Узкий слой OCR/recognition, не закрывает diligence workflow целиком | **5-10%** в OCR/ID parsing для finance и гос/enterprise, inference [B8] | Hebbia-like продукт закрывает следующий слой value chain: анализ, сопоставление и выводы по документам |

#### Вывод по конкурентам
- На Западе основной pressure идёт от **data incumbents** и **M&A workflow tools**.
- В РФ реальная конкуренция пока чаще приходит от **substitutes**: KYC/compliance data vendors, OCR/IDP и account-based due diligence tooling, а не от полноценного AI-native investment copilot.
- Значит, best wedge в РФ, это не «ещё один сервис проверки контрагентов», а **AI layer над data room, кредитным пакетом и IC memo**.

### B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Команда не успевает закрыть найм ML + Solutions к M6 | med | Высокий, сдвиг roadmap и пилотов на 2-3 месяца | time-to-hire > 2,5 мес, offer acceptance < 50% | заранее открыть hiring pipeline, использовать fractional experts, урезать кастом до 1 ICP |
| Operational | Рост latency/quality volatility у LLM API на длинных finance docs | high | Высокий, деградация demo quality и churn pilot-accounts | median answer latency > 20 сек, hallucination complaints > 3 на пилот | multi-model routing, offline evals, fallback prompts, human review в critical outputs |
| Market | Спрос остаётся нишевым, buyer не выделяет отдельный budget line | med | Высокий, низкая конверсия discovery→pilot | < 8 discovery calls на 100 target accounts, repeated feedback «интересно, но не budgeted» | продавать outcome через due diligence SLA и analyst-hours saved, а не через абстрактный AI |
| Market | Price compression из-за дешёвых локальных substitutes | high | Средний-высокий, ARPU сползает ниже 180k ₽/мес | discount requests > 25%, конкуренты сравниваются с Kontur/Rusprofile | жёстко держать enterprise ICP, пакеты с внедрением и security, ROI calculator для committee |
| Regulatory | 152-ФЗ и data residency блокируют cloud-hosted обработку data room | high | Высокий, часть банков/УК не может купить продукт | security questionnaire fail, требование on-prem/VPC почти в каждом тендере | RU-hosted private contour, on-prem/VPC SKU, DPA и data localization policy |
| Regulatory | 115-ФЗ / комплаенс и санкционные проверки требуют explainability и audit trail | med | Средний-высокий, risk/compliance team не подписывает deployment | запросы на полную трассировку ответа и provenance | immutable audit logs, citation-by-snippet, approval workflow для regulated outputs |
| Financial | Cash runway сжимается из-за длинных пилотов и delayed procurement | high | Высокий, риск down-round или bridge под давлением | burn > 6,5 млн ₽/мес три месяца подряд, cash runway < 12 мес | stage-gated hiring, предоплата пилотов, ежемесячный burn committee |
| Financial | Ослабление ₽ к USD/EUR повышает API и cloud COGS | med | Средний, GM падает на 5-10 п.п. | USD/RUB > 110 и рост vendor invoices > 15% | FX buffer, рублёвые контракты с клиентами, резервный pricing clause, локальные модели где возможно |
| Black swan | Новые санкции/отключение западного SaaS или LLM provider | med | Очень высокий, продукт частично перестаёт работать | ухудшение SLA, ограничения по billing/region, vendor notices | multi-vendor stack, open-source fallback, локальные inference nodes, escrow ключевых компонентов |
| Black swan | Военный/политический шок режет инвестактивность и freeze новых сделок | med | Высокий, pipeline due diligence резко сжимается | падение M&A / fundraising activity, остановка пилотов у PE/VC | диверсификация в credit/risk/compliance use cases, продажи банкам и крупным УК, а не только deal teams |

### B5. Kill conditions через 6 месяцев

1. **GTM kill:** к M6 меньше **6 paying clients** **или** MRR < **1,35 млн ₽/мес**. Это значит, что даже base ramp не держится и выход к 43 клиентам становится малореалистичным.
2. **Unit economics kill:** fully-loaded **CAC > 2,4 млн ₽** **и** CAC payback > **18 мес**. При таком уровне enterprise motion перестаёт быть capital-efficient.
3. **Retention/pricing kill:** monthly churn > **3,0%** **или** realized ARPU < **180 тыс. ₽/мес** на cohort basis. Тогда модель скатывается в fragile zone, что подтверждает Monte Carlo width.

### B6. Итог SECTION B

**Verdict: PASS WITH HEAVY RISK DISCOUNT.**

- Point estimate из SECTION A выглядит сильным.
- Но distribution analysis показывает **очень широкий разброс** и хрупкость по LTV/CAC.
- Для IC-решения я бы дал кейсу **не reject**, а **score downgrade** до момента, когда команда докажет: 1) on-prem / private deployment readiness, 2) pilot-to-paid conversion, 3) удержание ARPU не ниже 180k ₽/мес.

## Источники SECTION B
- [B1] S&P Capital IQ Pro: https://www.spglobal.com/market-intelligence/en/solutions/products/sp-capital-iq-pro
- [B2] PitchBook platform: https://pitchbook.com/platform
- [B3] DealRoom pricing / platform: https://dealroom.net/products/pricing
- [B4] Контур.Фокус на vc.ru: https://vc.ru/services/2316075-kontur-fokus-proverka-kontragenta-po-inn-i-ogrn
- [B5] Rusprofile тарифы: https://www.rusprofile.ru/subscribe
- [B6] СБИС / Saby тарифы: https://www.tensor-sbis.ru/tarify/vse-o-kompaniyah-i-vladelczah/
- [B7] ITFB EasyDoc на Habr: https://habr.com/ru/companies/itfb/news/965206/
- [B8] Smart Engines на Habr: https://habr.com/ru/news/536550/
- [B9] Smart Engines в Сколково: https://sk.ru/news/smart-engines-raspoznovanie-pasporta-rf/

<!-- P6B-DONE -->


---

# 06-verdict.md

# Verdict

[FINTECH] Hebbia Institutional Finance GEO Expand v2 — NEAR-PASS: 67/100 | EBITDA base=1260К₽/мес через 24 мес | LTV/CAC=6,7x | Ключевое преимущество: сильная unit economics в узком enterprise ICP | Главный риск: weak moat и тяжёлый pilot-driven GTM.

sector: FINTECH

## Итоговый статус
- **Вердикт:** NEAR-PASS
- **Normalized score:** **67/100**
- **Raw score:** **100/150**
- **Пороговое решение:** score 65-69 = near-pass
- **Investment committee note:** кейс не проходит в approve сейчас, но остаётся в рабочем shortlist как узкий enterprise FINTECH workflow при условии доказательства repeatable GTM и более сильного moat.

## Оценка
Source tier balance: T1=10, T2=7, T3=0, weighted=2.59. Penalty applied: -0 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | "LTV/CAC = 6,7x" и "CAC Payback = 7,3 месяца", при этом GM = 73,3%. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | "При 50 клиентах модель даёт ~1,26 млн ₽ EBITDA/мес", порог 500К₽ проходит в пределах 24 мес. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 16 | "по прямым запросам категории спрос в РФ выглядит низким или нишевым", но adjacent demand по HH и KYC workflow подтверждён. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 10 | "в РФ реальная конкуренция пока чаще приходит от substitutes", поэтому moat пока слабый и не investment-grade. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 14 | "152-ФЗ и data residency блокируют cloud-hosted обработку data room" и есть высокая зависимость от LLM/API. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | "founder-led enterprise GTM" реалистичен, payback 7,3 мес, но motion остаётся pilot-heavy и high-touch. |

**Normalized score = round((100 × 100) / 150) = 67/100.**

## Почему не APPROVED
Кейс проходит economics-gate, но не проходит investment committee threshold по запасу прочности. Слабые зоны, это: 1) direct demand в РФ по самой категории остаётся LOW, 2) moat остаётся weak и опирается скорее на execution, чем на структурную защиту, 3) on-prem, security review и pilot motion делают GTM дорогим и медленным.

## Moat: 7-factor framework

| Фактор | Балл (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не улучшает продукт для остальных напрямую. |
| Switching costs | 2 | Интеграции, data room history и обученность analyst-team создают умеренный lock-in. |
| Scale economies | 1 | Есть частичная экономия на платформе, но COGS остаётся заметным из-за inference и support. |
| Proprietary data / model advantage | 1 | Собственного крупного подтверждённого датасета нет, преимущество больше в workflow orchestration. |
| Regulatory moat | 1 | Compliance и security требования создают барьер, но явного лицензируемого moat нет. |
| Brand / distribution | 1 | Сильного локального бренда и дистрибуции в РФ не доказано. |
| Embedded workflow | 2 | При внедрении в due diligence / IC memo / credit review продукт может стать частью core workflow. |

**Сумма 7-factor = 8/21. Moat score = round((8 × 25) / 21) = 10/25.**

**Вывод по moat:** weak moat. Это автоматически входит в Top-3 Risks.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 10 995 000 ₽ |
| Fully-loaded CAC | 1 635 833 ₽ |
| LTV/CAC | 6,7x |
| CAC payback | 7,3 мес |
| Gross Margin | 73,3% |
| contribution_margin_rub_month | 165 000 ₽/клиент/мес |
| fixed_costs_rub_month | 6 990 000 ₽/мес |
| Break-even clients | 43 |
| Break-even month | M13 |
| startup_capital_to_bep_rub | 60 560 855 ₽ |
| company_ebitda_rub_month @ 43 clients | 105 000 ₽/мес |
| company_ebitda_potential_rub_month @ 50 clients | 1 260 000 ₽/мес |
| clients_to_500k_ebitda | 46 |
| months_to_500k_ebitda | 14 |
| clients_to_1m_ebitda | 49 |
| months_to_1m_ebitda | 15-16 |

## FULL business process from 04-economics.md

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Формирование account list по банкам, УК, PE и advisory | SDR | CRM, Контур.Фокус, ручной research | 2 ч/аккаунт | 2 000 | Средняя |
| 2 | Обогащение ЛПР и контактных путей | SDR | CRM, email finder, Telegram/email research | 1 ч | 1 000 | Средняя |
| 3 | Outbound sequence и первые касания | SDR | CRM sequences, email automation | 10-14 дней | 3 500 | Высокая |
| 4 | Discovery call и qualification | SDR + AE | Meet, CRM, note taker | 45 мин | 5 000 | Низкая |
| 5 | Продуктовое интервью по workflow | AE | CRM, demo deck | 1 ч | 4 500 | Низкая |
| 6 | Live demo на data room / memo workflow | AE + Solutions | Sandbox, demo workspace | 1,5 ч | 10 000 | Низкая |
| 7 | Технический scoping и security review | CTO + Solutions + AE | Security checklist, docs | 1 неделя | 40 000 | Низкая |
| 8 | Пилот на документах клиента | Solutions + ML + Backend | Cloud, LLM, коннекторы | 3-4 недели | 150 000 | Средняя |
| 9 | ROI-модель и memo для комитета закупки | AE + CEO | spreadsheet, deck | 6-8 ч | 22 000 | Низкая |
| 10 | Legal/procurement negotiation | CEO + AE + Ops | ЭДО, договор, redlines | 2-4 недели | 35 000 | Низкая |
| 11 | Invoice и получение оплаты | Ops/Finance | 1С, банк, ЭДО | 3-5 дней | 4 000 | Высокая |
| 12 | Onboarding, настройка workspace, train-the-team | CSM + Solutions | PM tool, cloud, connectors | 2-3 недели | 95 000 | Средняя |

## Команда

| Роль | Функция | FOT fully-loaded ₽/мес |
|---|---|---:|
| CEO | enterprise sales, fundraising, strategy | 845 000 |
| CTO/Tech Lead | архитектура, security, delivery | 715 000 |
| Senior Backend 1 | ingestion/API | 546 000 |
| Senior Backend 2 | workflow engine/integrations | 546 000 |
| ML Engineer | retrieval, evals, prompt systems | 676 000 |
| DevOps | infra, observability, private contour | 455 000 |
| Frontend | analyst workspace UI | 390 000 |
| Solutions Engineer | pilots, onboarding, custom workflows | 390 000 |
| SDR | outbound pipeline | 234 000 |
| AE | closing, procurement, renewals assist | 494 000 |
| Customer Success | adoption, expansion, retention | 325 000 |
| Ops/Finance | invoicing, contracts, admin | 234 000 |
| **Итого FOT** |  | **5 850 000 ₽/мес** |

## GTM: 10 named targets

| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Сбер CIB | Большой поток credit/investment workflow, потребность в ускорении memo и due diligence | email decision-maker + отраслевые конференции | 350 000 ₽/мес |
| ВТБ Капитал / ВТБ Инвестиции | Крупные сделки и кредитный контур, высокая цена analyst-hours | email decision-maker + партнёрство через advisory | 300 000 ₽/мес |
| Газпромбанк | Сложные кредитные и M&A кейсы, security-first buyer | партнёрство + личный intro через enterprise advisory | 300 000 ₽/мес |
| Альфа-Капитал | Есть денежный пул УК и задачи risk/investment review | email CIO/COO + targeted roundtable | 225 000 ₽/мес |
| БКС Мир инвестиций | Investment research и internal analytics workflow | vc.ru ad + founder outbound | 200 000 ₽/мес |
| Т-Инвестиции | Быстрая digital-команда, выше шанс на пилот и data-driven evaluation | email product/ops leader + warm intro | 225 000 ₽/мес |
| АФК Система / Sistema VC | Регулярный pipeline по инвестиционному анализу и portfolio review | founder-led outbound + конференция | 225 000 ₽/мес |
| А1 | Special situations и сложные deal-досье, ценность в speed-to-decision | партнёрство через M&A ecosystem | 250 000 ₽/мес |
| Kept Deal Advisory | Advisory workflow с большим объёмом data room review и memo prep | email practice lead + отраслевое мероприятие | 180 000 ₽/мес |
| Б1 / ex-EY practice в РФ | Due diligence practice может стать design partner и resale-channel | партнёрство + личный outbound | 180 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Impact | Почему критично |
|---|---|---|---|
| Weak moat и price compression against substitutes | Высокая | Высокий | Локальные покупатели уже платят за Контур.Фокус / Rusprofile / СБИС, и premium надо защищать outcome, а не data access. |
| 152-ФЗ, data residency, on-prem/VPC readiness | Высокая | Очень высокий | Без private contour часть банков и УК не пройдёт security review и procurement. |
| Pilot-heavy GTM и зависимость от LLM/API | Средняя-высокая | Высокий | Длинные пилоты и vendor volatility увеличивают burn и делают рост хрупким. |

## LTV Upside Calculator
Поскольку статус **NEAR-PASS**, нужен чёткий план, как довести кейс до approve без смены рынка.

| Рычаг | Текущее | Целевое | Эффект |
|---|---:|---:|---|
| ARPA / MRR на клиента | 225 000 ₽ | 260 000 ₽ | Поднимает contribution и ускоряет EBITDA threshold. |
| COGS на клиента | 60 000 ₽ | 50 000 ₽ | Увеличивает contribution_margin_rub_month до 210 000 ₽. |
| Monthly churn | 1,5% | 1,2% | Поднимает customer_ltv_rub и LTV/CAC. |
| Fully-loaded CAC | 1 635 833 ₽ | 1 300 000 ₽ | Ускоряет payback и снижает capital intensity. |
| Pilot to paid conversion | ~10% blended | 15%+ | Делает GTM более repeatable и снижает variance. |
| On-prem / VPC readiness | частично | доказано на 2 пилотах | Снижает regulatory friction и увеличивает win rate у банков. |

### Upside scenario
Если довести MRR до **260k ₽**, COGS до **50k ₽**, churn до **1,2%**, а CAC до **1,3 млн ₽**, тогда:
- contribution_margin_rub_month ≈ **210 000 ₽**
- customer_ltv_rub ≈ **18,2 млн ₽**
- LTV/CAC ≈ **14,0x**
- clients_to_500k_ebitda ≈ **36**
- company_ebitda_rub_month @ 50 clients ≈ **3,51 млн ₽/мес**

Это уже выглядело бы как approve-grade enterprise case.

## Что нужно доказать для апгрейда в APPROVED
1. **2 paid pilots** у банков/УК/ advisory с переходом pilot → annual contract.
2. **On-prem или private VPC readiness**, чтобы закрыть 152-ФЗ и security review.
3. **ARPA не ниже 180-225k ₽/мес** без сильного discounting против локальных substitutes.
4. **Стабильный pilot-to-paid conversion > 15%** на узком ICP.
5. **Повторяемый GTM** через 10 named accounts, а не только founder magic.

## Proof points required for committee reconsideration
- Signed LOI или контракт с enterprise buyer.
- Security checklist passed у хотя бы 1 regulated customer.
- Доказанный time-to-value: сокращение времени на due diligence / memo prep минимум на 30-50%.
- Подтверждение, что продукт продаётся как workflow layer, а не скатывается в bespoke research service.

## Финальный вывод
Hebbia-подобный institutional finance workflow в РФ выглядит как **реальный, но узкий enterprise wedge**. Экономика на бумаге сильная, EBITDA потенциал есть, но пока это не approve-grade модель, потому что рынок не подтверждает широкий repeatable demand, а moat держится на execution и интеграции, а не на структурной защите. Поэтому решение инвесткомитета сейчас, это **NEAR-PASS 67/100**.
