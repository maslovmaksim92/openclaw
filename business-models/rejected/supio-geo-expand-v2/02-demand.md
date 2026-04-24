---
stage: demand-validation
case: supio-geo-expand-v2
date: 2026-04-24
analyst: branch-models-lead
sector: LEGAL
verdict: REJECTED
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
Supio, plaintiff-side legal AI для claims, medical chronologies и demand workflow.

## Итог
**Статус: REJECTED на этапе demand validation.**

- Exact-demand в РФ по core-use-case слабый: все проверенные запросы через demand API дали **LOW**. [T2]
- В РФ есть широкий B2C legal traffic и онлайн-юридические сервисы, но почти нет подтверждения именно для plaintiff-side medical chronology + demand workflow как самостоятельного software category. [T1/T2]
- WTP существует у зарубежных legal AI игроков, но локальный российский рынок платит в основном за консультацию, досудебный пакет и сопровождение спора, а не за отдельный AI workflow layer для plaintiff litigation. [T1/T2]
- Profit Gate не проходит ни в одном из реалистичных monetization-сценариев: при доступном buyer universe и локальном price ceiling компания не дотягивает до **EBITDA 500 тыс. ₽/мес**. [T1/T2/T3]

## 1) Demand signals

### Demand API
- `legal ai demand letters medical chronology plaintiff litigation` → **LOW**, Google Trends RU 1, HH 0, Yandex Suggest 2. [T2]
- `досудебная претензия автоюрист` → **LOW**, Google Trends RU 0, HH 1, Yandex Suggest 2. [T2]
- `автоюрист телеграм бот` → **LOW**, Google Trends RU 1, HH 0, Yandex Suggest 2. [T2]
- `медицинская экспертиза для суда` → **LOW**, Google Trends RU 1, HH 15, Yandex Suggest 100. Это лучший локальный adjacent-signal, но он указывает скорее на рынок экспертиз и судебной медицины, а не на software pull по Supio-подобному продукту. [T2]
- `страховые споры юрист онлайн` → **LOW**, Google Trends RU 0, HH 3, Yandex Suggest 2. [T2]

### Интерпретация
- Локальный рынок подтверждает боль вокруг споров, претензий и медицинской экспертизы, но не подтверждает самостоятельный спрос на AI-платформу для plaintiff-side case assembly. [T2]
- В РФ этот workflow чаще упакован в услугу юриста, автоюриста, эксперта или подписку на правовую поддержку, а не в отдельный vertical SaaS. [T1/T2]
- Значит, продукту пришлось бы не собирать существующий спрос, а создавать новую категорию с длинным education cycle. [T2/T3]

## 2) Конкуренты и pricing anchors

### Зарубежные конкуренты
1. **Paxton AI**: `Individual` план стоит **$499/польз./мес** или **$2,999/год**; в описании прямо упомянуты *Medical Chronologies and Billing Summaries*. Это самый близкий публичный price anchor к medical-review workflow. [T1]
2. **CaseMark**: транскрибация **$5/час**, summaries/agent workflows **от $25 за запуск**, medical summaries **$0.10/страница**. Это подтверждает usage-based willingness to pay за litigation summary work. [T1]
3. **Clio Draft (ex-Lawyaw)**: **$99/польз./мес** при annual billing или **$109/польз./мес** monthly. Это не direct medical chronology tool, но реальный adjacent competitor по legal drafting automation. [T1]
4. **Supio**: pricing публично не раскрыт, продаётся через demo, pilot и enterprise-style packaging. Сам факт pilot motion подтверждает B2B WTP, но не даёт открытого price point. [T1]

### Локальные RU substitutes
1. **DestraLegal** продаёт досудебный пакет за **5 390 ₽**, судебный пакет за **8 990 ₽**, расширенный формат `Личный юрист` за **17 090 ₽**. Это сильный локальный якорь того, за что российский пользователь реально платит. [T2]
2. **ЕЮС**, **Правокард**, **Правовед.ru**, **100Юристов**, **Urist-24** продают или генерируют поток юридических обращений, но позиционируются как сервисы консультации и сопровождения, а не как plaintiff-litigation workflow software. [T1/T2]

### Вывод по pricing
- В США workflow AI может жить на чеке от **$99 до $499/seat/month** или usage-based тарифах. [T1]
- В РФ наблюдаемый willingness to pay ближе к **разовой услуге 5-17 тыс. ₽** на кейс/пакет, а не к дорогому recurring SaaS для law-firm ops. [T2]
- Для Supio-подобного motion это означает жёсткий локальный price compression. [T1/T2]

## 3) Telegram и RU-сервисы
- `Чат Юрист-Бот` прямо продвигает Telegram-бота: базовые консультации бесплатны, платные функции и сопровождение открываются внутри бота по запросу. Это B2C/legal-help motion, а не B2B plaintiff ops stack. [T2]
- `ЗаконБот` показывает consumer-facing сценарии: товар, ЖКХ, алименты, ДТП. Это подтверждает наличие спроса на быстрый юридический ответ в Telegram, но не на сложный litigation workflow. [T2]
- Demand API по `автоюрист телеграм бот` вернул **LOW**, subscribers signal отсутствует. [T2]

**Вывод:** Telegram в РФ уже занят low-ticket legal-help и lead-gen сценариями. Признаков платёжеспособного Telegram-first сегмента под Supio нет. [T2]

## 4) WTP, proof of willingness to pay

### Что подтверждено
- На глобальном рынке юристы реально платят за AI workflow automation: Clio Draft $99-109/seat/month, Paxton $499/seat/month, CaseMark usage-based pricing. [T1]
- В РФ платёжеспособность есть на уровне готовых юридических услуг и подписок: DestraLegal monetizes 5.4-17.1 тыс. ₽ за пакет; ЕЮС и Правокард масштабируют дистанционную поддержку и подписочный legal assistance. [T1/T2]

### Чего не хватает
- Нет открытых доказательств, что российские plaintiff/claims фирмы готовы платить recurring **100-300 тыс. ₽ MRR** именно за AI chronologies + demand workflow. [T1/T2]
- Нет видимого HH/job pull под аналогичный software layer в РФ. [T2]
- Нет локальных внедрений Supio-like tooling в публичном поле. [T2]

### Вывод по WTP
**WTP есть у adjacent legal automation и у юридических услуг, но не доказан для целевого Supio-use-case в РФ.** Поэтому локальную монетизацию приходится считать через пониженный чек и ограниченный buyer universe. [T1/T2/T3]

## 5) Buyers и bottom-up universe РФ

### 10 реальных потенциальных buyers / targets
1. Правовед.ru [T1]
2. DestraLegal [T2]
3. Европейская юридическая служба (ЕЮС) [T1]
4. Правокард [T1]
5. 100Юристов [T2]
6. Urist-24 [T2]
7. СберПраво [T2]
8. Amulex [T2]
9. Юрист для Людей [T2]
10. Автоюрист / страховые-споры boutique firms как отдельный сегмент, представленный множеством региональных игроков. [T3, спекуляция]

### Почему universe маленький
- В РФ нет развитого массового plaintiff-bar по американской модели с большим объёмом contingency-case assembly. [T3, спекуляция]
- Лучший локальный fit, по моей оценке, это не классические PI firms, а legal factories, подписочные юридические сервисы и claim-heavy consumer dispute operators. [T2/T3]
- Консервативно беру **30 организаций** в РФ, которые вообще могут быть адресуемыми для такого workflow, и только **40%** из них имеют достаточно объёма и процесса для recurring automation spend. Получаем **12 реальных buyers**. [T2/T3]

## 6) Market sizing

### Метод и допущения
- Курс для пересчёта: **1 USD = 74.8349 ₽** по странице ежедневных курсов Банка России на 24 апреля 2026 года. [T1]
- Базовый локальный чек для workflow SaaS беру как **75 тыс. ₽/мес** или **900 тыс. ₽/год** на клиента. Это заметно ниже US anchors и выше B2C one-off чеков, то есть компромисс между Clio/CaseMark/Paxton и локальным market reality. [T1/T2/T3]
- Для team/service hybrid сценария верхний разумный чек беру **150 тыс. ₽/мес** или **1.8 млн ₽/год**, но не использую его как baseline, чтобы не завышать рынок. [T2/T3]

### Top-down
- Отталкиваюсь от того, что в РФ платный спрос концентрируется не в mass plaintiff litigation, а в broader legal-assistance и dispute-resolution сервисах. По данным ЕЮС, сервис работает с **250+ юристами** и масштабной клиентской базой; Правокард заявляет **6.5+ млн клиентов** и **900+ специалистов**; Правовед.ru говорит о **2 221 143** рекомендующих пользователях. Это подтверждает, что деньги в legal-demand есть, но они сосредоточены в сервисных платформах, а не в узком plaintiff SaaS. [T1/T2]
- Консервативно беру только **30 адресуемых компаний/операторов**, из которых 12 попадают в сегмент fit. При baseline ARR **0.9 млн ₽** получаем **SAM top-down = 10.8 млн ₽/год**. [T2/T3]
- Если считать весь более широкий legal-service universe, получился бы больший рынок, но для Supio это был бы искусственный overreach. Поэтому я intentionally режу TAM до ближайшего practical wedge. [T2/T3]

### Bottom-up
- 10 целевых buyers выше.
- Из них реально нуждающихся и готовых пилотировать продукт в первый год, по моей оценке, **3 компании**. [T2/T3]
- ARR на аккаунт: **0.9 млн ₽/год**. [T1/T2/T3]
- Получаем **SAM bottom-up = 10 × 0.9 = 9.0 млн ₽/год**.
- **SOM Y1 bottom-up = 2 клиента × 0.9 = 1.8 млн ₽/год**.
- **SOM Y3 bottom-up = 4 клиента × 0.9 = 3.6 млн ₽/год**.

### Таблица reconciliation

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 90-170 млрд ₽ [T3, LOW CONFIDENCE] | — | открытых T1/T2 для точной vertical оценки не найдено | top-down range |
| TAM (РФ) | 27.0 млн ₽ [T2/T3] | 18.0 млн ₽ [T2/T3] | diff=1.5x, top-down включает весь практический wedge, bottom-up только 10 первичных targets | **18.0 млн ₽** |
| SAM (РФ) | 10.8 млн ₽ [T2/T3] | 9.0 млн ₽ [T2/T3] | diff=1.2x, расхождение умеренное | **9.0 млн ₽** |
| SOM Y1 | 2.7 млн ₽ | 1.8 млн ₽ | diff=1.5x | **1.8 млн ₽** |
| SOM Y3 | 5.4 млн ₽ | 3.6 млн ₽ | diff=1.5x | **3.6 млн ₽** |

### Sanity-check
- Расхождение top-down и bottom-up меньше 3x, значит оценка внутренне согласована. [T2/T3]
- SOM Y1 = 1.8 млн ₽, это **20%** от preferred SAM, что уже выглядит агрессивно для новой категории. Это red flag. [T3]
- При среднем sales cycle 4-6 месяцев закрыть 2 клиента за первый год ещё возможно, но масштабировать до 4 клиентов к Y3 без сильного category proof всё равно тяжело. [T3]

## 7) Profit Gate, проверка всех monetization scenarios

### Сценарий A: solo/seat SaaS
- Цена: **25 тыс. ₽/мес**
- Валовая маржа: **80%**
- Реалистичное число платящих аккаунтов: **до 6** в ближайшем обозримом рынке. [T2/T3]
- EBITDA до fixed opex: `25 × 6 × 0.8 = 120 тыс. ₽/мес`.
- **Итог:** сильно ниже порога 500 тыс. ₽/мес. FAIL. [T3]

### Сценарий B: team workflow SaaS
- Цена: **75 тыс. ₽/мес**
- Валовая маржа: **70%**
- Реалистичное число аккаунтов: **3-4**. [T2/T3]
- EBITDA proxy: `75 × 4 × 0.7 = 210 тыс. ₽/мес` до fixed opex.
- **Итог:** порог 500 тыс. ₽/мес не достигается. FAIL. [T3]

### Сценарий C: service-heavy hybrid
- Цена: **150 тыс. ₽/мес**
- Валовая маржа: **45%** из-за ручной работы по medical review / demand packaging. [T3]
- Реалистичное число аккаунтов: **2-3**. [T2/T3]
- EBITDA proxy: `150 × 3 × 0.45 = 202.5 тыс. ₽/мес` до fixed opex.
- **Итог:** даже с высоким чеком не проходит из-за низкой маржи и маленького buyer pool. FAIL. [T3]

### Общий вывод по Profit Gate
**Profit Gate FAIL.** Даже лучший реалистичный сценарий не выводит компанию на **EBITDA 500 тыс. ₽/мес** в РФ-сегменте Supio-like plaintiff workflow. [T2/T3]

## 8) Основные риски
1. Неподходящая рыночная структура: в РФ нет сильного plaintiff-bar аналога США. [T3, спекуляция]
2. Спрос сидит в услуге, а не в отдельном workflow-SaaS. [T1/T2]
3. Локальный price ceiling низкий относительно US legal AI products. [T1/T2]
4. Buyer universe очень ограничен, и он уже привык либо к подписке на юрподдержку, либо к per-case fee. [T1/T2]
5. Telegram layer в РФ monetizes low-ticket support, но не решает B2B economics. [T2]

## 9) Решение для pipeline
**EARLY REJECT:** выполнено условие `DEMAND = LOW` и `Profit Gate FAIL`.

Рекомендация: записать verdict как **REJECTED** и перевести кейс в `pipeline/rejected/`.

## Источники
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=legal%20ai%20demand%20letters%20medical%20chronology%20plaintiff%20litigation [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%B4%D0%BE%D1%81%D1%83%D0%B4%D0%B5%D0%B1%D0%BD%D0%B0%D1%8F%20%D0%BF%D1%80%D0%B5%D1%82%D0%B5%D0%BD%D0%B7%D0%B8%D1%8F%20%D0%B0%D0%B2%D1%82%D0%BE%D1%8E%D1%80%D0%B8%D1%81%D1%82 [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%B0%D0%B2%D1%82%D0%BE%D1%8E%D1%80%D0%B8%D1%81%D1%82%20%D1%82%D0%B5%D0%BB%D0%B5%D0%B3%D1%80%D0%B0%D0%BC%20%D0%B1%D0%BE%D1%82 [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BC%D0%B5%D0%B4%D0%B8%D1%86%D0%B8%D0%BD%D1%81%D0%BA%D0%B0%D1%8F%20%D1%8D%D0%BA%D1%81%D0%BF%D0%B5%D1%80%D1%82%D0%B8%D0%B7%D0%B0%20%D0%B4%D0%BB%D1%8F%20%D1%81%D1%83%D0%B4%D0%B0 [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D1%81%D1%82%D1%80%D0%B0%D1%85%D0%BE%D0%B2%D1%8B%D0%B5%20%D1%81%D0%BF%D0%BE%D1%80%D1%8B%20%D1%8E%D1%80%D0%B8%D1%81%D1%82%20%D0%BE%D0%BD%D0%BB%D0%B0%D0%B9%D0%BD [T2]
- Supio pricing: https://www.supio.com/pricing [T1]
- Paxton pricing: https://www.paxton.ai/pricing [T1]
- CaseMark pricing: https://casemark.com/pricing [T1]
- Clio Draft pricing: https://www.clio.com/draft/pricing/ [T1]
- DestraLegal: https://destralegal.ru/ [T2]
- Правовед.ru: https://pravoved.ru/ [T1]
- ЕЮС: https://els24.com/ [T1]
- Правокард: https://pravocard.ru/ [T1]
- 100Юристов: https://100yuristov.com/ [T2]
- Urist-24: https://urist-24.com/ [T2]
- Банк России, ежедневные курсы валют: https://www.cbr.ru/currency_base/daily/ [T1]

Sources: T1=8, T2=8, T3=1. Primary evidence basis: T1/T2.
