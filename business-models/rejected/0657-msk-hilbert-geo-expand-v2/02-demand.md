# 02-demand

## Demand validation summary

**Компания / гипотеза:** Hilbert как warehouse-native AI decisioning / CDP-подобный слой для growth, CRM и персонализации B2C-команд при geo-expand в РФ.

**Итог P4:** **DEMAND = LOW**, **WTP = MEDIUM**, **Profit Gate = FAIL**.

Ключевая причина: в РФ есть подтверждённая потребность в CRM-маркетинге и продуктовой аналитике, но не в виде отдельной новой enterprise-платформы уровня Hilbert. Спрос размазан между уже установленными стеками, локальными CRM/CDP и Telegram-first automation. Для иностранного нового вендора вход осложняют data localization, procurement и наличие локальных платформ, уже продающих сегментацию, journeys, Telegram/VK/SMS и аналитику. 

## External demand signals

- API `multi-demand` по ключу `customer data platform` вернул `composite_demand=LOW`, `demand_score=18`, `hh_vacancies=28`, `yandex_suggest=100`, `google_trends_ru=0`. [T1 for HH slice via API, internal demand endpoint]
- API `multi-demand` по ключу `CRM-маркетинг` вернул `composite_demand=LOW`, `demand_score=26`, `hh_vacancies=266`, `yandex_suggest=100`, `google_trends_ru=0`. Это лучше отражает локальный JTBD, чем англоязычный CDP-термин. [T1]
- API `multi-demand` по ключу `product analytics` вернул `composite_demand=LOW`, `demand_score=22`, `hh_vacancies=136`. [T1]
- На hh.ru по запросу `CRM-маркетинг` найдено **311 вакансий** по состоянию на 2026-04-20, что подтверждает наличие функции, но не обязательно нового budget line под ещё один stack. [T1] https://hh.ru/search/vacancy?text=CRM-%D0%BC%D0%B0%D1%80%D0%BA%D0%B5%D1%82%D0%B8%D0%BD%D0%B3

**Вывод:** спрос на outcome есть, но он выражен как CRM-маркетинг / retention / personalization внутри существующих систем, а не как очевидный pull на новый warehouse-native AI decisioning vendor. Это важное различие.

## Competitor pricing and WTP proof

### Глобальные аналоги с публичной ценой

1. **Mixpanel**: Growth plan, после 1 млн событий, **$0.28 за 1k events**; free tier до 1 млн monthly events. Это прямое доказательство оплаты за product/growth analytics. [T1] https://mixpanel.com/pricing/
2. **PostHog**: Product analytics после free tier, **$0.0000500/event** для диапазона 1-2 млн событий. [T1] https://posthog.com/pricing
3. **BotHelp**: Pro от **$18/мес**, таблица до **$995/мес** на 300k subscribers. Это не full Hilbert competitor, но важный RU/Eastern Europe proof, что компании платят за automated messaging + Telegram/Viber/WhatsApp layer. [T2] https://bothelp.io/
4. **RetailCRM**: тариф **от 9 360 ₽/мес** с маркетингом на данных, лояльностью, чатами и мессенджер-маркетингом. [T2] https://www.retailcrm.ru/prices
5. **Heap**: free до 10k monthly sessions, дальше **custom session pricing**. Публичный price floor есть, но enterprise monetization скрыта. [T1] https://www.heap.io/pricing

### Конвертация в ₽

Курс ЦБ РФ на 2026-04-18: **1 USD = 76.0535 ₽**. [T1] https://www.cbr-xml-daily.ru/daily_json.js

- Mixpanel: $0.28 / 1k events ≈ **21.30 ₽ / 1k events** [T1]
- PostHog: $0.0000500/event ≈ **0.0038 ₽/event** или **3.80 ₽ / 1k events** [T1]
- BotHelp Pro floor: $18/мес ≈ **1 369 ₽/мес** [T2+T1 FX]

### WTP assessment

**WTP = MEDIUM, не HIGH.**

Почему не HIGH:
- Есть реальная готовность платить за analytics/CDP/automation стек, что видно по Mixpanel, PostHog, RetailCRM и BotHelp. [T1/T2]
- Но в РФ budget чаще уходит в **already bundled platforms**: CRM, loyalty, messaging automation, CDP, email/push/Telegram orchestration. [T2]
- Для Hilbert нужен отдельный budget line поверх warehouse, BI, CRM, push/email stack и data team. Это повышает friction и удлиняет цикл сделки. [Inference from T1/T2]

## Russian Telegram bots / services check

В РФ и русскоязычном контуре уже есть сервисы, которые частично закрывают ценностное предложение Hilbert через Telegram-first automation, CRM journeys и messaging:

- **RetailCRM**: прямо заявляет мессенджер-маркетинг, Telegram, VK и visual scenarios. [T2] https://www.retailcrm.ru/prices
- **Altcraft Platform**: заявляет CDP, customer journey automation, ML/best send time, рассылки в Telegram/Viber/WhatsApp и on-prem deployment. [T2] https://altcraft.com/ru
- **BotHelp**: Telegram/Viber/WhatsApp automation, pricing прозрачен и low-friction. [T2] https://bothelp.io/

**Следствие:** Telegram в РФ не white space, а уже занят локальными инструментами. Для Hilbert это одновременно канал дистрибуции и риск commoditization. [Inference from T2]

## Market sizing

### Методология

Сделаны оба пути, top-down и bottom-up. Оценка низкой/средней уверенности, потому что прямой открытый T1-источник именно по RU CDP/decisioning сегменту ограничен.

### База для расчёта

- Объём интернет-торговли в РФ в 2024 году: **9 трлн ₽**, доля e-commerce в рознице **16.2%**. [T2] АКИТ / отраслевые публикации, данные 2024 года.
- hh.ru показывает 311 вакансий по `CRM-маркетинг`, что подтверждает активный слой работодателей, где retention/personalization реально финансируются. [T1]
- В РФ уже продаются локальные платформы CRM/CDP/маркетинг automation с Telegram-каналом, значит spending line на этот класс задач существует. [T2]
- Для мирового TAM используется публичный внешний market estimate по CDP / product analytics классу как ориентир, **[LOW CONFIDENCE]**. [T3]

### Top-down

Предпосылки:
- TAM world для смежного CDP / customer intelligence класса: **~8 млрд $** как внешний ориентир, не как точная цифра. [T3, LOW CONFIDENCE]
- TAM RF: берём e-commerce 9 трлн ₽ и addressable software+data+personalization spend **0.04%** от GMV для enterprise/mid-market use cases. Это даёт **3.6 млрд ₽**. [Inference anchored on T2]
- SAM RF: берём 60% от TAM RF, оставляя только mid-market/enterprise buyers с event volume, data team и performance marketing maturity. Получаем **2.16 млрд ₽**. [Inference from T1/T2]
- SOM Y1: 2% от SAM = **43.2 млн ₽**. [Model assumption]
- SOM Y3: 7% от SAM = **151.2 млн ₽**. [Model assumption]

### Bottom-up

10 реальных buyers для ICP: **Ozon, Wildberries, Lamoda, Детский мир, Лэтуаль, Золотое Яблоко, Hoff, ВсеИнструменты.ру, М.Видео-Эльдорадо, Купер**. [T2, representative buyer set]

Предпосылки:
- Total buyers в релевантном ICP по РФ: **~1 000** крупных и средних B2C digital / e-commerce / omnichannel игроков, где есть CRM, product analytics и собственные performance teams. [T2/T3, LOW CONFIDENCE]
- % with need: **35%**, опираясь на слой вакансий `CRM-маркетинг` и наличие локальных CDP/automation platforms. [T1/T2]
- ARR avg: **6 млн ₽/год** на один mid-market/enterprise контракт, то есть ~500k ₽ MRR. Это консистентно с enterprise motion между low-end SaaS и high-touch platform sale. [Inference from T1/T2 competitor price floors]

Расчёт:
- SAM bottom-up = 1 000 × 35% × 6 млн ₽ = **2.1 млрд ₽**
- SOM bottom-up Y1 = 2.1 млрд ₽ × 2% = **42 млн ₽**
- SOM bottom-up Y3 = 2.1 млрд ₽ × 7% = **147 млн ₽**

### Reconciliation table

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | ~8 млрд $ [T3, LOW CONFIDENCE] | — | — | top-down |
| TAM (РФ) | 3.6 млрд ₽ [T2 + inference] | 6.0 млрд ₽ [T2/T3 + inference, 1 000 buyers × 100% × 6 млн ₽] | diff 1.7x, допустимо для молодого сегмента | **3.6 млрд ₽** |
| SAM (РФ) | 2.16 млрд ₽ [T1/T2 + inference] | 2.1 млрд ₽ [T1/T2 + inference] | diff 1.03x, хорошее совпадение | **2.1 млрд ₽** |
| SOM Y1 | 43.2 млн ₽ | 42.0 млн ₽ | diff 2.8% | **42.0 млн ₽** |
| SOM Y3 | 151.2 млн ₽ | 147.0 млн ₽ | diff 2.9% | **147.0 млн ₽** |

**Sanity checks:**
- SOM Y1 < 10% SAM, значит не выглядит overclaiming.
- При среднем enterprise deal cycle 6-9 месяцев закрытие выручки уровня ~42 млн ₽ в год 1 потребует около 7 клиентов по 6 млн ₽ ARR или эквивалентный mix, что уже тяжело для нового foreign entrant. [Inference]

## Profit Gate: может ли компания выйти на EBITDA >= 500k ₽/мес?

Проверены все базовые сценарии.

### Сценарий A: SMB/self-serve analytics
- Price: 50k ₽ MRR
- Gross margin: 80%
- Opex для локального sales + solutions + support + legal/data compliance: минимум 2.0-2.5 млн ₽/мес [Inference]
- Для EBITDA 500k ₽/мес нужен валовой вклад ~2.5-3.0 млн ₽/мес, то есть **63-75 платящих клиентов**.
- Для RU-enterprise-like analytics продукта это нереалистично. 

**Вердикт:** FAIL.

### Сценарий B: Mid-market platform
- Price: 150k-300k ₽ MRR
- Берём midpoint 225k ₽ MRR
- Gross contribution на клиента при 80% margin ≈ 180k ₽/мес
- Для EBITDA 500k ₽/мес при Opex 2.5 млн ₽/мес нужно ~3.0 млн ₽ contribution, то есть **17 клиентов**.
- С учётом длинного onboarding, need for local trust и competition с bundled local suites это выглядит тяжело. [Inference from T2]

**Вердикт:** FAIL / borderline.

### Сценарий C: Enterprise/high-touch CDP-decisioning
- Price: 500k-900k ₽ MRR
- Берём midpoint 700k ₽ MRR
- Contribution при 75% margin ≈ 525k ₽/мес на клиента
- Для EBITDA 500k ₽/мес при Opex 3.5 млн ₽/мес нужно около **8 клиентов**.
- Экономически это единственный вменяемый путь, но он конфликтует с реальностью рынка: локальные игроки уже продают аналогичный stack, enterprise sales cycles 9-12 месяцев, нужен on-prem / data localization / локальная поддержка. [T2 + inference]

**Вердикт:** FAIL в горизонте входа на рынок.

### Итог Profit Gate

**Profit Gate = FAIL.** Теоретически 500k ₽ EBITDA/мес достижимы только в enterprise-сценарии, но practically not achievable для нового foreign entrant без локальной инфраструктуры, партнёрской сети и сильного wedge. 

## Final judgment

- **Demand:** LOW
- **WTP:** MEDIUM
- **Telegram / RU substitutes:** PRESENT and strong
- **Profit Gate:** FAIL

Согласно правилу раннего отклонения, комбинация **DEMAND=LOW + Profit Gate FAIL** означает **REJECT NOW**.

Sources: T1=6, T2=5, T3=2. Primary evidence basis: T1/T2.