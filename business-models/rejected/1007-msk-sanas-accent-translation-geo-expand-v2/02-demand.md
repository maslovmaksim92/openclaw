# 02-demand — Demand Validation

## Кейс
1007-msk-sanas-accent-translation-geo-expand-v2

## Итог
**Статус: EARLY REJECT**

Глобальный traction у Sanas сильный, но в РФ и русскоязычном контуре самостоятельный спрос на accent translation для контакт-центров остаётся слишком узким. Exact demand по category-запросам в `multi-demand` нулевой, а платёжеспособность подтверждается в основном у adjacent voice/contact-center stack, не у отдельного budget line именно под accent translation.

## 1. Demand data
Источник exact keyword: `http://172.18.0.1:9001/multi-demand?keyword=sanas%20accent%20translation`

- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **0**
- Habr articles: **2**
- hh.ru vacancies: **0**
- Yandex suggest: **2**
- Telegram subscribers detected automatically: **0**

Дополнительные смежные проверки:

### `accent translation contact center`
- Composite demand: **LOW**
- Demand score: **0**
- Google Trends RU: **1**
- hh.ru vacancies: **0**
- Yandex suggest: **2**

### `contact center ai`
- Composite demand: **LOW**
- Demand score: **15**
- Google Trends RU: **1**
- hh.ru vacancies: **2**
- Yandex suggest: **100**

### `call center english`
- Composite demand: **LOW**
- Demand score: **11**
- hh.ru vacancies: **476**
- Google Trends RU: **1**
- Yandex suggest: **2**

### Интерпретация
- Прямой спрос на category-level формулировку в РФ практически не виден.
- Смежный спрос есть не на accent translation как продукт, а на **англоязычный support** и более широкий **contact center AI**.
- Это подтверждает существование боли, но не подтверждает, что рынок уже готов массово покупать отдельный accent-translation layer.

## 2. Реальные конкуренты и ценовые якоря

| Игрок | Что продаёт | Публичная цена | Вывод |
|---|---|---:|---|
| Sanas | Real-time speech AI platform для accent translation, language translation, speech enhancement | **цена не публична, demo / sales-led motion** | Сильный enterprise signal, но отсутствие прозрачного pricing указывает на тяжёлый custom-sales motion |
| Krisp | Accent conversion и call center AI | Accent Conversion есть в платных планах, call center AI продаётся через sales | Accent conversion существует как feature-layer, а не обязательно как standalone большая категория |
| Deepgram | Voice Agent API и speech stack | **$0.075/мин** Voice Agent API, STT **$0.0077–0.0165/мин** | Голосовой AI-слой уже commoditized на API-уровне, что давит на ценовой ceiling |
| MANGO OFFICE | Омниканальный контакт-центр в РФ | **7 800 / 10 200 / 13 400 ₽/мес**, доп. функции и роботы отдельно | В РФ подтверждён бюджет на contact-center stack, но не на дорогой отдельный accent-translation wedge |

## 3. Product / traction validation
По официальным материалам Sanas:
- платформа уже продаёт **Accent Translation**, **Language Translation** и **Speech Enhancement**;
- среди вертикалей заявлены **healthcare, financial services, retail, travel**;
- компания пишет о **750 000+ users globally** после Series B в 2025;
- customer story с **TP (Teleperformance)** показывает enterprise deployment и заявленные эффекты **+22% CSAT**, **-37.5% AHT**, **+14% FCR**.

### Вывод по traction
Это сильное доказательство, что технология **реальна и коммерциализируема глобально**. Но для demand-stage в РФ этого недостаточно: global proof не равен local category readiness.

## 4. Российский контур и substitutes
В локальном контуре деньги уже тратятся на:
- контакт-центры,
- омниканальные inbox/voice platforms,
- речевую аналитику,
- голосовых роботов,
- quality monitoring и workforce management.

Однако явного локального контура, где компании отдельно покупают именно **accent translation** как самостоятельный software/service budget line, не видно.

### Вывод
В РФ это выглядит скорее как:
- feature inside broader CCaaS / voice stack,
- enterprise add-on для очень узкого слоя BPO и multilingual support,
- либо custom enterprise rollout с длинным циклом продаж.

## 5. TAM / SAM / SOM в рублях

### Базовые допущения
- Беру консервативный целевой сегмент: международные контакт-центры, travel, hospitality, medical tourism, outsourcing/BPO и enterprise support-команды с заметным англоязычным voice-volume.
- Средний реалистичный контракт для РФ/CIS беру **150 000 ₽/мес** = **1 800 000 ₽/год** на клиента. Это уже премиальный add-on относительно локальных contact-center тарифов.

### TAM
Из 5 000+ контакт-центров на Mango и более широкого enterprise voice-контура релевантным для accent translation выглядит только узкий слой. Беру **400** компаний как широкий верхний контур.

**TAM = 400 × 1 800 000 ₽ = 720 млн ₽/год**

### SAM
Реально адресуемый первый слой, где есть англоязычный inbound/outbound voice, offshore support или международный service desk: **120** компаний.

**SAM = 120 × 1 800 000 ₽ = 216 млн ₽/год**

### SOM
Ранний реалистичный слой для нового игрока в регионе: **8 контрактов**.

**SOM = 8 × 1 800 000 ₽ = 14.4 млн ₽/год**

### Вывод по рынку
Рынок не нулевой, но слишком узкий для fund-level standalone wedge. Это скорее niche enterprise capability, чем большой самостоятельный category build в РФ.

## 6. WTP, готовность платить
Что подтверждено:
1. Компании уже платят за контакт-центр и voice automation stack.
2. Глобальные enterprise buyers готовы покупать Sanas в крупном BPO/enterprise контуре.
3. В РФ есть бюджеты на voice tooling, роботов, QA и аналитику.

Что не подтверждено:
1. Что российский рынок выделяет отдельный значимый бюджет именно под **accent translation**.
2. Что buyer воспринимает это как must-have wedge, а не nice-to-have improvement.
3. Что локальный рынок потянет premium pricing при наличии более дешёвых substitutes в broader voice stack.

### Вывод по WTP
**Adjacent WTP подтверждён, category-specific WTP не доказан.**

## 7. Profit Gate
Нужен путь к **EBITDA ≥ 500 000 ₽/мес**.

### Сценарий A. Add-on per seat
- Средний аккаунт: **20 операторов**
- Цена: **6 000 ₽ за seat/мес**
- MRR на клиента: **120 000 ₽**
- GM: **55%**
- Валовая прибыль на клиента: **66 000 ₽/мес**
- Для fixed costs **1.8 млн ₽/мес** нужно **35+ клиентов**

**Вердикт: FAIL**

### Сценарий B. Usage-based speech layer
- Цена: эквивалент **3–5 ₽/мин** в локальном бюджете после конкурентного давления
- При GM **30–35%** для EBITDA 500k нужен слишком большой monthly volume
- Для niche сегмента multilingual contact centers это выглядит нереалистично

**Вердикт: FAIL**

### Сценарий C. Managed enterprise rollout
- Цена: **250 000 ₽/мес**
- GM: **25%** из-за enterprise onboarding, integrations и support
- Валовая прибыль на клиента: **62 500 ₽/мес**
- Для fixed costs **2.0 млн ₽/мес** нужно **40 клиентов**

**Вердикт: FAIL**

## 8. Общий вывод
- Exact search demand: **почти отсутствует**
- Adjacent demand: **есть, но не category-specific**
- Глобальный traction: **сильный**
- РФ budget line для accent translation: **не доказан**
- Profit Gate: **не проходит**

## 9. Решение для пайплайна
**Отклонить на этапе demand validation.**

Sanas подтверждает, что технология и глобальный enterprise use case реальны. Но как standalone кейс для РФ/СНГ это пока слишком узкий, дорогой и sales-heavy wedge без доказанного локального спроса, достаточного для fund-level upside.

## Market Pulse
Market Pulse 19.04.2026: умеренный глобальный рост интереса, но локальный РФ-сигнал слабый.

## Источники
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=sanas%20accent%20translation
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=accent%20translation%20contact%20center
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=contact%20center%20ai
- Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=call%20center%20english
- Sanas homepage: https://www.sanas.ai/
- Sanas About Us: https://www.sanas.ai/about-us
- Sanas customer story with TP: https://www.sanas.ai/customer-stories/tp
- Krisp pricing: https://krisp.ai/pricing/
- Deepgram pricing: https://deepgram.com/pricing
- MANGO OFFICE contact center: https://www.mango-office.ru/products/contact-center/
- MANGO OFFICE tariffs: https://2flk.mango-office.ru/products/contact-center/tariffs/

Обновление Market Pulse 20.04.2026: растущий интерес.

По текущим веб-сигналам у speech AI и real-time translation вышли свежие продуктовые анонсы, но локальный РФ-сигнал по-прежнему слабее глобального.

> Market Pulse 2026-04-20: растущий интерес.
