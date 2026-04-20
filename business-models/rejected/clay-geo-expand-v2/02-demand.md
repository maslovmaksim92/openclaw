# 02-demand

## Вывод
**Решение: REJECTED (early reject).**

Причина: по обязательному demand-check сигнал слабый, а profit gate на уровне компании (EBITDA >= 500 000 ₽/мес) не проходит ни в одном реалистичном сценарии для РФ. Запрос на Clay-подобный AI-native GTM stack в России существует, но выглядит нишевым, фрагментированным и чаще закрывается ручным сервисом, Telegram-инструментами или более дешёвыми альтернативами, а не отдельной platform spend. [T1][T2]

## Demand snapshot
- `multi-demand` по ключу `Clay sales enrichment outbound automation` вернул **LOW**: demand_score=0, hh_ru vacancies=0, Habr articles=2, Yandex suggest score=2, Google Trends RU score=1. Это прямой отрицательный сигнал на локальный осознанный спрос именно в форме product category. [T2]
- Clay как продукт подтверждает WTP на западном рынке, но это ещё не равняется локальному buyer pull в РФ. На странице Clay есть платный Launch-план **$167/мес**, а также кейсы OpenAI, Anthropic, Rippling, Verkada и Intercom, что подтверждает наличие платящей аудитории за рубежом. [T2]
- В РФ есть смежный спрос на Telegram/offline leadgen-инструменты, но ценовой коридор ниже: Telemetr Premium **4 900 ₽/мес**, TargetHunter bot **1 250 ₽/мес**, KMLeads «Инвайт» **10 000 ₽/мес**. Это подтверждает наличие рынка performance/leadgen tooling, но одновременно задаёт низкий anchor price для массового сегмента. [T2]

## Конкуренты и цены
### Глобальные прямые/квазипрямые конкуренты
1. **Clay**: Launch от **$167/мес**. Позиционирование: enrichment, signals, workflows, email sequencing. [T2]
2. **Apollo.io**: Basic **$49/мес**, Professional **$99/мес**, Enterprise, contact sales. Позиционирование: sales intelligence + sequencing + database. [T2]
3. **Snov.io**: Starter с monthly price anchor **$39/мес** (в HTML pricing), отдельный add-on LinkedIn automation **$62–69/мес per slot**. [T2]

### Локальные RU/TG-смежные сервисы
1. **Telemetr Premium**: **4 900 ₽/мес**. Telegram analytics / monitoring / discovery. [T2]
2. **KMLeads**: пакет «Инвайт» **10 000 ₽/мес**. Telegram-аудитория и автоматические приглашения. [T2]
3. **TargetHunter bot**: **1 250 ₽/мес**. Массовый audience tooling / bot-first acquisition workflow. [T2]

**Интерпретация:** конкурентное поле в РФ есть, но локальный ценовой якорь сильно ниже enterprise GTM stack spend. Для Clay-like решения это означает тяжёлое обучение рынка и high-touch продажу без очевидного product-led pull. [T2]

## WTP, proof of willingness to pay
- **Положительное доказательство WTP вне РФ:** Clay публикует customer proof и платные тарифы; Apollo и Snov.io также имеют прозрачные recurring plans. Это показывает, что budget line «sales intelligence / enrichment / outbound automation» как класс существует. [T2]
- **Ограничение для РФ:** локальные альтернативы чаще продают point solutions в коридоре **1 250–10 000 ₽/мес**, а не unified GTM operating system. Это снижает готовность платить за «platform + workflow + enrichment» без явного ROI-кейса и без локальных data providers. [T2]
- **Вывод по WTP для РФ:** willingness to pay есть только у узкого слоя B2B-tech / enterprise revenue teams и агентств-операторов; для массового рынка подтверждений на recurring spend уровня 150–300k ₽/мес на tooling не найдено. **WTP = selective, not broad.** [T2]

## Telegram / RU channel check
- В РФ существует выраженный слой Telegram-native инструментов для поиска каналов, аудиторий, сигналов и приглашений: Telemetr, KMLeads, TargetHunter bot. [T2]
- Но это не полноценная замена Clay: они решают discovery / audience / outreach fragments, а не multi-source B2B data enrichment и workflow orchestration. [T2]
- Для GEO-expand в РФ это означает не пустой рынок, а наоборот «рынок с дешёвыми substitutes», где buyer уже привык покупать отдельные utility tools, а не дорогую orchestration platform. [T2]

## Адресат и 10 реальных buyers для bottom-up
Ниже не «все покупатели», а стартовый ICP для service-led захода: крупные B2B vendors, облака, интеграторы, enterprise-агентства и data-heavy команды продаж. Это реальные компании, у которых есть outbound, партнёрские продажи или ABM-модель. [T2]
1. Яндекс Cloud [T2]
2. Selectel [T2]
3. VK Tech [T2]
4. MTS Web Services [T2]
5. SberCloud [T2]
6. Контур [T2]
7. Softline [T2]
8. IBS [T2]
9. КРОК [T2]
10. iConText Group / Kokoc Group-type B2B performance operators [T2]

## Market sizing [LOW CONFIDENCE]
### Методика
Считал **только service-led / enterprise operator** сценарий для РФ, а не «весь martech». Иначе top-down сильно завышает адресуемый рынок относительно реального buyer readiness. [T2]

### Допущения
- Плановый FX для перевода глобальных цен и сопоставления: **90 ₽/$** (модельное допущение для investment memo, не биржевая котировка). [Inference]
- Узкий ICP в РФ: примерно **15 000 компаний** с реальным B2B outbound / ABM / SDR / revenue operations контуром. Это не весь МСП-рынок, а верхний слой software vendors, облаков, интеграторов, B2B agencies, enterprise suppliers. [T2]
- Доля с подтверждённой болью: **8–12%**, берём **10%**. Аргумент: низкий multi-demand score и отсутствие заметного hh/поискового volume по самой категории. [T2]
- Средний чек service-led Clay-like implementation+ops: **600 000 ₽/год** на клиента в базовом сценарии, что эквивалентно ~50 000 ₽/мес software+ops attach или нескольким спринтам оператора. Для enterprise-heavy пакета возможен чек **1,8–3,0 млн ₽/год**, но не как массовая база. [T2]

### Таблица market sizing
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 315 млрд ₽, если взять ~35 млн knowledge/revenue workers globally × 1% addressable × 10 000 ₽/мес tooling+ops [T2][Inference] | — | — | top-down |
| TAM (РФ) | 9,7 млрд ₽ = 15 000 компаний × 54 000 ₽/мес потенциального full-stack spend [T2][Inference] | 10,8 млрд ₽ = 15 000 × 60 000 ₽/мес [T2][Inference] | diff ~11%, допустимо, bottom-up чуть выше из-за более высокого ARPA | lower |
| SAM (РФ) | 1,08 млрд ₽ = 9,7 млрд ₽ × 11% pain-fit [T2][Inference] | 900 млн ₽ = 15 000 × 10% × 600 000 ₽/год [T2][Inference] | diff ~20%, допустимо | lower |
| SOM Y1 | 18 млн ₽ = 1,08 млрд ₽ × 1,7% [Inference] | 18 млн ₽ = 900 млн ₽ × 2% [Inference] | близко | **используем 18 млн ₽** |
| SOM Y3 | 63 млн ₽ = 1,08 млрд ₽ × 5,8% [Inference] | 54 млн ₽ = 900 млн ₽ × 6% [Inference] | diff ~17% | **используем 54 млн ₽** |

### Комментарий к sizing
- Расхождение между top-down и bottom-up меньше 3x, поэтому модель можно считать внутренне согласованной. [Inference]
- **Но это не software TAM Clay в РФ.** Это только адресуемый service-led/operator слой при узком ICP. [Inference]
- Даже при таком узком SAM рынок не выглядит достаточно «горячим» для дешёвого GTM: потребуются кастомные продажи, data integrations и ручная поставка результата. [T2]

## Profit gate: проверка всех сценариев
### Сценарий A, software resale / light implementation
- 10 клиентов × 50 000 ₽/мес = 500 000 ₽ выручки/мес. [Inference]
- Для поставки нужны минимум founder-sales + revops/operator + partial data engineer/support. Даже при очень lean setup фонд оплаты и overhead съедают почти всю валовую прибыль. EBITDA **< 150 000 ₽/мес**. [Inference]
- **FAIL.**

### Сценарий B, managed outbound / operator layer
- 4 клиента × 180 000 ₽/мес = 720 000 ₽ выручки/мес. [Inference]
- Для качественной поставки нужны 2–3 оператора + SDR/research + аккаунт. С учётом data subscriptions и management load EBITDA обычно **100 000–250 000 ₽/мес**. [Inference]
- **FAIL.**

### Сценарий C, enterprise package
- 2 клиента × 300 000 ₽/мес = 600 000 ₽ выручки/мес. [Inference]
- В реальности 2 enterprise аккаунта дают высокий delivery risk, длинный цикл сделки и кастомную интеграцию. EBITDA чаще **около нуля или низкая положительная** до выхода на 4–5 клиентов. [Inference]
- **FAIL.**

### Сценарий D, best-case hybrid
- 3 enterprise клиента × 250 000 ₽/мес + 3 mid-market клиента × 90 000 ₽/мес = 1 020 000 ₽ выручки/мес. [Inference]
- Такой портфель уже требует полноценной команды delivery/research/ops, т.е. почти маленького агентства. Реалистичный EBITDA диапазон **200 000–400 000 ₽/мес**, всё ещё ниже порога 500 000 ₽/мес. [Inference]
- **FAIL.**

**Итог по profit gate:** во всех разумных сценариях EBITDA компании **ниже 500 000 ₽/мес**. Чтобы пройти порог, нужен либо существенно более высокий локальный WTP, либо уникальный proprietary data moat, которого в brief не видно. [Inference]

## Почему reject сейчас
1. **Demand = LOW** по обязательному external signal API. [T2]
2. Локальный рынок уже закрывает часть боли дешёвыми Telegram/point solutions, что ограничивает willingness to pay за «единый Clay-слой». [T2]
3. Service-led модель может собрать выручку, но не показывает убедимый путь к EBITDA >= 500 000 ₽/мес без агентского масштаба и тяжёлой delivery-команды. [Inference]
4. Зависимость от западного data stack, phone/email enrichment и third-party sources делает GEO-expand в РФ операционно хрупким. [T2]

## Что должно измениться для re-open
- Появятся 3–5 подтверждённых российских enterprise-клиентов с чеком **>=250 000 ₽/мес** именно за GTM orchestration/enrichment, а не за разовый лидоген. [T2]
- Появится локальный data moat или API bundle, который нельзя быстро собрать из Telemetr/KMLeads/ручного ресёрча. [T2]
- Появятся доказательства, что delivery можно стандартизировать до gross margin, совместимой с EBITDA >500k/мес при 4–6 клиентах. [Inference]

Sources: T1=0, T2=12, T3=0. Primary evidence basis: T2.