---
stage: demand-validation
case: superdial-geo-expand-v2
date: 2026-04-23
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: REJECTED
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
SuperDial, AI-автоматизация телефонных звонков клиник и billing-команд страховщикам в healthcare revenue cycle.

## Итог
**Решение на этапе demand validation: REJECTED.**

Почему early reject:
- Обязательный internal demand endpoint по релевантным RU-ключам вернул **LOW**: `автоматизация звонков клиники страховщикам` = demand_score 0, `автообзвон клиники` = 0, `медицинский колл-центр автоматизация` = 3. Это значит, что в РФ нет заметного публичного спроса именно на такой wedge. [T2]
- В РФ есть спрос на более широкий слой автоматизации коммуникаций клиники, но он смещён в front-desk, запись, напоминания и Telegram/мессенджеры, а не в payer/billing phone workflows по модели США. [T2]
- Реальные публичные прайсы у конкурентов и локальных substitute-решений указывают на низкий или средний чек. При этих чеках кейс **не проходит Profit Gate**: EBITDA компании >= 500 тыс. ₽/мес. не достигается ни в одном реалистичном сценарии без слишком большого числа клиентов и сервисной нагрузки. [T1][T2]

## Demand signals

### 1) Обязательный demand endpoint
Проверка 23.04.2026:
- `автоматизация звонков клиники страховщикам` → `LOW`, score 0, hh.ru 0, Google Trends RU 0, Habr 2, Yandex Suggest 2. [T2]
- `медицинский колл-центр автоматизация` → `LOW`, score 3, hh.ru 33, Google Trends RU 0, Habr 2, Yandex Suggest 2. [T2]
- `автообзвон клиники` → `LOW`, score 0, hh.ru 0, Google Trends RU 0, Habr 2, Yandex Suggest 2. [T2]

Вывод: базовая боль вокруг call-center automation у клиник существует, но exact-demand под специализированный payer-facing voice RCM workflow в РФ слабый. [T2]

### 2) Что реально покупают в РФ
Локальные игроки продают не revenue-cycle calling как в США, а:
- голосового AI-администратора и пропущенные звонки для клиник,
- запись на приём,
- подтверждения и напоминания,
- коммуникации через Telegram/WhatsApp,
- первичный intake и квалификацию пациента. [T2]

Это важная развилка: продуктовый рынок в РФ есть, но он уже уже и дешевле, чем core-use-case SuperDial. [T2]

## Конкуренты и цены

### Глобальные/смежные конкуренты с публичными ценами
1. **Smith.ai**: AI receptionist from **$97.50/мес**, далее планы **$292.50**, **$825**, **$2475** в месяц. Это верхняя вилka generic receptionist/answering, не healthcare-RCM-only. [T1]
2. **Dialzara**: **$29 / $99 / $199** в месяц, overage **$0.48/min**. Это very low-end benchmark по рынку AI receptionist. [T1]
3. **Goodcall**: публично заявляет старт **от $59/мес**. [T1]

### Локальные RU substitute-решения
1. **ZoeAgent**: на сайте указаны пакеты **от 3 490 ₽/мес** до **22 490 ₽/мес** для AI-администратора/бота. [T2]
2. **1Meda**: фокус на автоматизацию записи и коммуникаций клиник; публичный сайт подтверждает 50+ внедрений, но без открытого тарифа, что делает ценовой сигнал неполным. [T2]
3. **Telegram-first bots / студийные внедрения**: рынок РФ насыщен кастомными ботами для записи и поддержки, обычно продающимися как low-ticket внедрение + подписка, а не как дорогой RCM platform layer. [T3, спекуляция]

### Что это значит для WTP
- Даже верхняя публичная глобальная вилка generic AI receptionist редко выглядит как очевидный контракт > 500 тыс. ₽/мес. на одного клиента. [T1]
- В РФ публичные цены ещё ниже, обычно на уровне **3.5–22.5 тыс. ₽/мес.** за front-desk automation. [T2]
- Чтобы пройти EBITDA gate, нужен либо enterprise workflow с многомодульным чеком, либо очень высокая плотность клиентов. Для payer-calling wedge в РФ ни первое, ни второе пока не подтверждено. [T2]

## Telegram в РФ
Проверка RU-ландшафта показывает, что рынок уходит в мессенджерный интерфейс, а не в сложный insurer-calling workflow:
- у российских сервисов для клиник Telegram обычно используется как канал записи, напоминаний, FAQ и уведомлений, а не как ядро revenue-cycle automation; [T2]
- это снижает ценность сложного голосового b2b2payer стека и давит на ARPU; [T2]
- для buyer-а в РФ Telegram-бот часто выглядит достаточным substitute для части задач front-desk. [T2]

## WTP, willingness to pay

### Подтверждения готовности платить
- Глобально бизнесы платят за AI receptionist / answering software по подписке от десятков до сотен долларов в месяц, иногда до low-thousands для более насыщенных plans. Это доказывает **наличие WTP**, но не на уровне крупного enterprise RCM stack по умолчанию. [T1]
- В РФ клиники уже платят за автоматизацию записи и коммуникаций, но публичные вилки на local-market сайтах ближе к low-ticket SaaS, чем к high-LTV enterprise budget line. [T2]

### Вывод по WTP
**WTP подтверждён, но WTP низкий/средний, не fund-return grade для данного wedge в РФ.** [T1][T2]

## Market sizing

### Логика сегментации
Оцениваю не весь medtech и не весь private healthcare, а только слой автоматизации звонков / front-desk / patient communications, который можно реально продать в РФ как substitute SuperDial. Поскольку американский insurance-claims workflow в РФ выражен слабее, беру консервативный сегмент. [T2]

### Исходные допущения
- Базовый рынок: частная медицина РФ. Публичные отраслевые обзоры оценивают рынок платных медуслуг в России примерно в **1.4–1.5 трлн ₽**. [T2]
- Публичные компании показывают масштаб потенциальных buyers: у **MD Medical** 14 госпиталей и 76 клиник в 35 регионах, то есть крупные сетевые операторы реально существуют. [T1]
- Крупные сети вроде EMC работают 24/7 call-first и явно несут операционную нагрузку на коммуникации. [T2]
- Для голосовой/коммуникационной автоматизации беру addressable share **0.3%** от оборота частной медицины как консервативную оценку software+service spend, из которого только часть подходит под узкий wedge SuperDial. Это modelling assumption, а не прямая наблюдаемая метрика. [T2, допущение]

### Таблица cross-check
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 315 млрд ₽ экв. (~$3.5 млрд global conversational AI in healthcare, грубый proxy) [T3] | — | — | top-down |
| TAM (РФ) | 4.2 млрд ₽ = 1.4 трлн ₽ × 0.3% [T2] | 3.0 млрд ₽ = 10 000 клиник/сетевых юнитов × 300 тыс. ₽ ARR [T2] | diff ~1.4x, допустимо; беру lower | **3.0 млрд ₽** |
| SAM (РФ) | 1.26 млрд ₽ = TAM × 30% для частных сетей/клиник с заметным inbound volume [T2] | 720 млн ₽ = 3 000 buyers × 240 тыс. ₽ ARR [T2] | diff ~1.75x; беру lower | **720 млн ₽** |
| SOM Y1 | 14.4 млн ₽ = 1.26 млрд ₽ × 1.1% [T2] | 7.2 млн ₽ = 720 млн ₽ × 1% [T2] | diff 2x; используем lower | **7.2 млн ₽** |
| SOM Y3 | 63 млн ₽ = 1.26 млрд ₽ × 5% [T2] | 36 млн ₽ = 720 млн ₽ × 5% [T2] | diff 1.75x; используем lower | **36 млн ₽** |

### Bottom-up buyers
10 реальных buyer-групп, на которые такой продукт теоретически можно продавать в РФ:
1. MD Medical / «Мать и дитя» [T1]
2. EMC [T2]
3. Медси [T2]
4. СМ-Клиника [T2]
5. Будь Здоров [T2]
6. Скандинавия / АВА-ПЕТЕР [T2]
7. Поликлиника.ру [T2]
8. Инвитро [T2]
9. Гемотест [T2]
10. KDL [T2]

### Почему SAM ограничен
- Не все клиники имеют объём звонков, достаточный для отдельного voice AI stack. [T2]
- Российский рынок слабее зависит от phone-based payer claim status workflows, чем рынок США. [T2]
- Часть спроса закрывается Telegram-ботами, CRM-модулями и обычным колл-центром. [T2]
- Слишком высокий enterprise ACV здесь плохо подтверждён публичными прайсами. [T1][T2]

## Profit Gate
Цель: проверить, может ли компания выйти на **EBITDA >= 500 тыс. ₽/мес.** в РФ.

### Сценарий A. Low-ticket SaaS
- 20 клиентов × 15 000 ₽/мес = 300 000 ₽ MRR. [T2]
- Даже при gross margin 80% это далеко ниже целевого EBITDA после sales/support/integration. [T2]
- **FAIL**.

### Сценарий B. Mid-market voice automation
- 10 клиентов × 50 000 ₽/мес = 500 000 ₽ MRR. [T2]
- Для payer-facing healthcare workflow в РФ такой средний чек уже агрессивен относительно публичных substitute prices. [T1][T2]
- При founder + sales + customer success + telephony/LLM costs EBITDA всё ещё около нуля или отрицательная. [T2]
- **FAIL**.

### Сценарий C. Enterprise managed rollout
- 5 клиентов × 150 000 ₽/мес = 750 000 ₽ MRR. [T2]
- На бумаге revenue выглядит лучше, но для такого чека нужны доказанные интеграции, комплаенс, SLA и сложный workflow beyond reception. В РФ это публично не подтверждено. [T2]
- Даже если 1-2 сделки возможны, повторяемость слабая, а sales cycle длинный. [T2]
- **FAIL / слишком спекулятивно**.

### Вывод по Profit Gate
**Profit Gate FAIL.** На локальном рынке чётко подтверждается спрос на дешёвую или среднюю автоматизацию коммуникаций, но не на тот high-LTV payer-calling wedge, который нужен для EBITDA >= 500 тыс. ₽/мес. как устойчивого бизнеса. [T1][T2]

## Риски
- Основной use-case SuperDial исторически завязан на американский healthcare RCM, а не на российскую модель частной медицины. [T2]
- Локальные substitute-решения дешевы, что создаёт сильный price ceiling. [T1][T2]
- Telegram и обычные чат/CRM-инструменты отъедают часть value pool. [T2]

## Вывод
Кейс выглядит как **интересный вертикальный сигнал**, но не как сильный GEO-EXPAND-кандидат для РФ. Спрос низкий именно по нужному wedge, willingness-to-pay ограничен, а пройти Profit Gate на локальном рынке не получается.

**Итог: early reject на этапе Demand Validation.**

## Источники
- Smith.ai pricing: https://smith.ai/pricing/ai-receptionists [T1]
- Dialzara pricing: https://dialzara.com/pricing [T1]
- Goodcall pricing: https://www.goodcall.com/pricing [T1]
- ZoeAgent pricing: https://zoeagent.ru/ [T2]
- 1Meda: https://1meda.ru/ [T2]
- MD Medical about: https://www.mcclinics.ru/about/ [T1]
- EMC about / call-center evidence: https://www.emcmos.ru/about/ [T2]
- Internal multi-demand endpoint, проверки 23.04.2026 [T2]
- Grand View Research, conversational AI in healthcare proxy: https://www.grandviewresearch.com/industry-analysis/conversational-ai-in-healthcare-market-report [T3]

Sources: T1=4, T2=5, T3=1. Primary evidence basis: T2.
