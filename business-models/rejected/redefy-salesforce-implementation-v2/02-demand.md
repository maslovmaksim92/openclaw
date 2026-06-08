---
stage: demand-validation
case: redefy-salesforce-implementation-v2
date: 2026-04-21
analyst: branch-models-lead
sector: B2B-OPS
verdict: PASS_WITH_RESERVATIONS
confidence: medium
---

> Market Pulse 2026-04-25: растущий интерес.

# 02-demand — Demand Validation

## Кейс
ReDEFY, AI-native оператор внедрения Salesforce Agentforce и смежного enterprise стека.

## Итог
**Решение на этапе demand validation: PASS WITH RESERVATIONS.**

- По прямым локальным запросам спрос в РФ выглядит **LOW**: `Salesforce implementation`, `Salesforce consulting`, `Agentforce`, `Salesforce Agentforce`, `Salesforce CRM внедрение`, `внедрение Salesforce` не показывают сильного inbound-пула. [T2]
- Но это не означает отсутствия бюджета. ReDEFY прямо продаёт себя как consulting partner, который сжимает внедрение Salesforce с месяцев до недель, а его оффер включает implementation, integration, optimization и managed services. То есть кейс бьёт не в новый SMB-поиск, а в уже существующий enterprise budget line вокруг крупных CRM / service / industry deployments. [T1]
- Salesforce официально показывает, что Agentforce монетизируется как отдельный enterprise слой: add-ons от **$125-150 за пользователя в месяц**, Agentforce 1 Editions от **$550 за пользователя в месяц**, а consumption-модель продаётся через Flex Credits. Это сильный anchor, что вокруг платформы уже существует дорогой software spend, на который могут наслаиваться внедренческие услуги. [T1]
- Поэтому ранний reject по правилу `LOW demand + Profit Gate FAIL` пока не срабатывает. Для узкого enterprise motion c implementation + managed services путь к EBITDA выше 500 тыс. ₽/мес выглядит реалистичным, но только при высоком ACV и жёстком контроле кастома. [T1][T2][inference]

## 1) Спрос и сигналы рынка

### Demand API
- `Salesforce implementation` → LOW, score 0, HH vacancies 2, Google Trends RU 1, Yandex suggest 2. [T2]
- `Salesforce consulting` → LOW, score 3, HH vacancies 10, Google Trends RU 0, Yandex suggest 2. [T2]
- `Agentforce` → LOW, score 15, HH vacancies 2, Google Trends RU 0, Yandex suggest 100. [T2]
- `Salesforce Agentforce` → LOW, score 0, HH vacancies 0, Yandex suggest 2. [T2]
- `Salesforce CRM внедрение` → LOW, score 3, HH vacancies 17, Google Trends RU 0, Yandex suggest 2. [T2]
- `внедрение Salesforce` → LOW, score 3, HH vacancies 20, Yandex suggest 2. [T2]

### Интерпретация
- В РФ нет заметного search-led спроса именно на категорию Salesforce / Agentforce implementation. [T2]
- Но кейс и не должен продаваться через широкий поисковый спрос. Это enterprise services motion поверх уже выбранной платформы, где бюджет появляется после решения о стеке, а не через самостоятельный category search. [T1][inference]
- Наличие вакансий и Yandex suggest по `Agentforce` показывает ранний интерес к теме, но пока ещё не зрелый локальный рынок. [T2]

## 2) Category proof и бюджетный якорь

1. ReDEFY прямо заявляет, что это **"the first Salesforce consulting partner built around AI delivery"**, и обещает делать Agentforce deployments reliable at scale, compress Salesforce implementations from months to weeks и deliver measurable outcomes from day one. Это подтверждает наличие понятного JTBD: ускорение и де-рискинг дорогих enterprise-внедрений. [T1]
2. На сайте ReDEFY перечислены коммерчески понятные услуги: **Salesforce Strategy and Roadmapping**, **Salesforce Implementation and Integration**, **Salesforce Optimization and Managed Services**, а также AWS/Salesforce integration. Это важный сигнал, что выручка может складываться не из одного разового проекта, а из land-and-expand модели. [T1]
3. Salesforce официально публикует прайсинг Agentforce: employee-facing add-ons от **$125/user/month**, industries add-ons от **$150/user/month**, Agentforce 1 Editions от **$550/user/month**, плюс consumption-модель **$500 за 100k Flex Credits**. Это означает, что базовая software линия сама по себе дорогая и допускает дорогую implementation economics. [T1]
4. Следовательно, рынок для такого оператора, это не "внедрение CRM вообще", а узкий слой компаний, уже готовых платить за Salesforce + Agentforce и не желающих проходить долгий SI-цикл. [T1][T2][inference]

## 3) WTP и willingness to pay

### Прямые сигналы WTP
- Salesforce уже монетизирует Agentforce отдельными add-ons и edition-level лицензиями, что подтверждает высокий software ACV в верхнем сегменте enterprise accounts. [T1]
- ReDEFY продаёт не bodyshopping, а ускорение внедрения, валидацию конфигурации, отраслевую экспертизу и managed services. Это означает, что покупатель может платить не только за лицензии, но и за speed-to-value. [T1]
- В combined motion лицензии + integration + optimization + support дают правдоподобный путь к чеку, достаточному для сервисной EBITDA. [T1][inference]

### Оценка WTP
- Для малого рынка РФ Salesforce-сигнал сам по себе слабый, поэтому mass-market WTP низкий. [T2]
- Для enterprise buyer, уже сидящего на Salesforce или планирующего Agentforce rollout, проектный чек **3-8 млн ₽** и дальнейший managed-services контракт **300-800 тыс. ₽/мес** выглядят правдоподобно. Это inference из публичного Salesforce pricing и структуры услуг ReDEFY, а не подтверждённый прайс-лист интегратора. [T1][inference]
- Значит, willingness to pay есть, но только в узком слое крупных аккаунтов. [T1][T2]

## 4) TAM / SAM / SOM в рублях

### Подход и допущения
- Считаю только РФ GEO-EXPAND слой для enterprise Salesforce / Agentforce implementation motion.
- Целевой buyer universe беру как **80 аккаунтов**: крупные банки, телекомы, high-tech, industrial, professional services и другие enterprise-компании, где Salesforce и смежные cloud-стэки экономически возможны. [T1][T2][inference]
- Средний годовой revenue на аккаунт для оператора беру **6,0 млн ₽**: сочетание initial implementation и/или managed services. [T1][inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---:|
| TAM (РФ) | **720 млн ₽** = 120 потенциальных enterprise accounts × 6,0 млн ₽ [T1][T2][inference] | **480 млн ₽** = 80 accounts × 6,0 млн ₽ [T1][T2][inference] | diff=1,5x, допустимо для раннего enterprise sizing | **480 млн ₽** |
| SAM (РФ) | **216 млн ₽** = 30% TAM [inference] | **180 млн ₽** = 30 deployable accounts × 6,0 млн ₽ [T1][T2][inference] | почти сходится | **180 млн ₽** |
| SOM Y1 | **12,0 млн ₽** = 2 accounts × 6,0 млн ₽ [inference] | **12,0 млн ₽** = 2 accounts × 6,0 млн ₽ [inference] | полное совпадение | **12,0 млн ₽** |
| SOM Y3 | **36,0 млн ₽** = 6 accounts × 6,0 млн ₽ [inference] | **36,0 млн ₽** = 6 accounts × 6,0 млн ₽ [inference] | полное совпадение | **36,0 млн ₽** |

### 10 реальных buyers для bottom-up
1. Сбер
2. ВТБ
3. Альфа-Банк
4. Т-Банк
5. МТС
6. МегаФон
7. Ростелеком
8. Северсталь
9. Норникель
10. Яндекс

Все 10, это inference как типы крупных enterprise-аккаунтов, где возможен дорогой CRM / service / industry rollout; это не подтверждение текущего Salesforce-контракта. [inference]

## 5) Profit Gate

### Сценарий A. Разовый project-only SI
- Initial чек **2,0 млн ₽**, без заметного follow-on support. [inference]
- Модель слишком проектная и нестабильная, прибыльность будет рваной. [inference]
- **Profit Gate: BORDERLINE FAIL.**

### Сценарий B. Implementation + managed services
- Initial чек **4-6 млн ₽** плюс **300-500 тыс. ₽/мес** сопровождения. [T1][inference]
- 4-6 активных аккаунтов уже могут давать выручку, достаточную для EBITDA >500 тыс. ₽/мес при компактной delivery-команде. [inference]
- **Profit Gate: PASS.**

### Сценарий C. AI-native premium operator
- Initial чек **6-10 млн ₽** плюс **500-800 тыс. ₽/мес** managed services / optimization / governance. [T1][inference]
- При 3-5 клиентах экономика выглядит сильной, если AI-слой реально сокращает delivery hours и не превращается в обычный консалтинг. [T1][inference]
- **Profit Gate: STRONG PASS.**

## 6) Ключевые риски
- Локальный прямой спрос слабый, поэтому продажи будут зависеть от partner-led и outbound motion, а не от organic inbound. [T2]
- Высокий риск, что обещание "AI-native delivery" не даст достаточного unit-economics преимущества и кейс скатится в обычный SI business с дорогими людьми. [T1][inference]
- Узкий buyer pool ограничивает SOM, а длинный enterprise sales cycle растягивает cash conversion. [T1][T2][inference]
- Зависимость от Salesforce ecosystem повышает platform risk: если вендор и традиционные SI-партнёры быстро закроют gap, дифференциация оператора сузится. [T1][inference]

## 7) Вывод для pipeline
Кейс не подтверждает широкий локальный search demand, но подтверждает наличие дорогого enterprise budget layer вокруг Salesforce Agentforce, на который может сесть AI-native implementation operator. Для РФ это не массовый сервисный рынок, а узкий B2B-OPS enterprise motion с высокими чеками и малым числом покупателей.

**Решение на этапе demand validation: PASS WITH RESERVATIONS.**

На P4/P5 нужно особенно жёстко проверить repeatability delivery model, долю кастома, CAC через partner / founder-led sales и то, действительно ли AI-среда даёт сокращение сроков настолько, чтобы удерживать премиальную маржу.

## Источники
- ReDEFY homepage, accessed 2026-04-21: https://redefy.com/ [T1]
- Salesforce Agentforce pricing, accessed 2026-04-21: https://www.salesforce.com/agentforce/pricing/ [T1]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=Salesforce%20implementation [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=Salesforce%20consulting [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=Agentforce [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=Salesforce%20Agentforce [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=Salesforce%20CRM%20%D0%B2%D0%BD%D0%B5%D0%B4%D1%80%D0%B5%D0%BD%D0%B8%D0%B5 [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%B2%D0%BD%D0%B5%D0%B4%D1%80%D0%B5%D0%BD%D0%B8%D0%B5%20Salesforce [T2]

Sources: T1=2, T2=6, T3=0. Primary evidence basis: T1/T2.
## Market Pulse
- Market Pulse 2026-04-21: узкий enterprise budget layer подтверждён, массовый inbound не подтверждён.

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.
Market Pulse 22.04.2026: растущий интерес.

> Market Pulse 2026-04-23: растущий интерес.
> Market Pulse 2026-04-24: растущий интерес.

> Market Pulse 2026-04-26: растущий интерес.

> Market Pulse 2026-05-11: растущий интерес. По текущей веб-выдаче по ключевым запросам виден рост публикаций, вакансий и/или vendor-активности.


> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по ключевым запросам сохраняются свежие публикации, вакансии и/или vendor-активность.

> Market Pulse 2026-05-13: растущий интерес. По текущей веб-выдаче по ключевому запросу видна свежая рыночная активность.
