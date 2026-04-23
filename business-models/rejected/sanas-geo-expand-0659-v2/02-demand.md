# Demand validation

## Итог
**Вердикт по спросу: LOW.** Как отдельный market container для РФ кейс слабый и схлопывается в более широкий customer service operations. Явный pain есть только у узкого слоя компаний с международным voice-трафиком, а не у массового российского контакт-центра.

## Demand signals
- Российский рынок облачных контакт-центров в 2024 году составил **2,7 млрд ₽**, а в 2025 году ожидается около **3,5 млрд ₽** [T2, TMT Consulting, https://tmt-consulting.ru/napravleniya/telekommunikacii/tmt-rejting-rossijskij-rynok-oblachnyx-kontakt-centrov-itogi-2024-goda/].
- Один только MANGO OFFICE заявляет **5000+ контакт-центров на платформе**; это подтверждает наличие широкой базовой инфраструктуры, но не доказывает отдельный большой слой именно для accent translation [T2, MANGO OFFICE, https://www.mango-office.ru/products/contact-center/].
- На HH.ru спрос на операторов колл-центра в целом высокий, но bilingual/English voice-support встречается штучно; это косвенно показывает, что pain по снятию акцента и переводу есть лишь у узкой ниши, а не у всего рынка [T1, HH.ru search pages, supporting evidence].
- Обязательная проверка `http://172.18.0.1:9001/multi-demand?keyword=Sanas accent translation call center` выполнена, но endpoint дважды вернул **timeout без данных**. Использовать его как evidence не удалось.

## Конкуренты с ценами
1. **Krisp**: на pricing-странице видны планы **$15/польз./мес. при annual** и **$30/польз./мес. monthly**; это нижняя граница для voice enhancement / call-center adjacent tooling [T2, https://krisp.ai/pricing/].
2. **TalkTool**: landing и SERP-данные показывают пакет около **$299/мес.** и overage порядка **$0.25/мин.** для live call translation [T2/T3, https://www.usetalktool.com/].
3. **ExpatPhone**: публичное позиционирование around **€0.27/мин.** для call translation; ближе к usage-based модели [T3, https://expatphone.app/].
4. **SpeechTranslate**: публичные прайс-упоминания around **$0.99/мин.**; это скорее high-friction benchmark, чем массовый SMB SaaS [T3, public pricing mentions].

**Вывод по pricing:** рыночные аналоги либо seat-based по относительно умеренной цене, либо per-minute и быстро становятся дорогими. Для РФ это ограничивает объём покупателей, готовых внедрять продукт как отдельную категорию.

## Telegram и RU services
- **Speakly Bot** в Telegram делает перевод голосовых сообщений, поддерживает 70+ языков и Pro-режим; это real product, но ориентирован на B2C/B2SMB коммуникацию, а не на enterprise contact center stack [T2, https://speakly.bot/ru/].
- На российском рынке есть Telegram-боты и consumer-style сервисы для перевода голосовых, но они закрывают разовые voice notes, а не QA, routing, agent desktop и compliance-интеграции контакт-центра [T2/T3].
- Прямого широко известного RU-лидера именно в **real-time accent translation for contact centers** не найдено; локальные игроки обычно ближе к speech analytics, ASR, QA и voicebots, а не к Sanas-like layer [T2, market reading; partly speculative].

## WTP, willingness to pay
- Исходный кейс уже содержал диапазон **1,2–6,0 млн ₽ в год на mid-market / enterprise аккаунт**; беру его как внутренний рабочий benchmark, согласующийся с внешними seat-based аналогами [internal brief + T2/T3 competitor pricing].
- Для 30 агентов по модели Krisp annual аналог стоит примерно **$5,400/год**, то есть порядка **0,49 млн ₽/год** при курсе около 90 ₽/$; enterprise-layer с кастомной интеграцией может подняться до **1,2–2,4 млн ₽/год** [T1 CBR FX reference; T2 competitor pricing; inference].
- Готовность платить в РФ подтверждается только для узких use-cases: международные BPO, travel, hospitality, экспортные sales/support команды. Массовой evidence-базы по русскоязычному domestic contact center нет [T1/T2].

## Market sizing
### Допущения
- Addressable share для accent translation внутри рынка облачных КЦ: **1–3%**. Это отражает очень узкий bilingual/multilingual voice слой [inference from T2 market size + T1 HH scarcity].
- Segment fit для standalone продукта: **60%** от addressable слоя, так как часть компаний решит задачу процессом, наймом bilingual-операторов или ручным переводом.
- Реалистичный capture: **Y1 = 3% SAM**, **Y3 = 10% SAM**.

### Top-down
- TAM РФ = **3,5 млрд ₽ × 1–3% = 35–105 млн ₽** [T2]. Для preferred беру **35 млн ₽** как консервативную границу.
- SAM РФ = **35 млн ₽ × 60% = 21 млн ₽**.
- SOM Y1 = **0,63 млн ₽**.
- SOM Y3 = **2,1 млн ₽**.

### Bottom-up
- Базовая инфраструктура: **5000+ контакт-центров** только у одного крупного провайдера [T2].
- Для Sanas-like pain беру **0,4–0,8%** от этой базы как компании с реальным международным voice-трафиком и готовностью платить за снятие акцента/перевод, то есть **20–40 покупателей** [T1/T2 + inference].
- Средний контракт: **1,2–1,8 млн ₽/год** [internal brief + competitor benchmarks].
- SAM bottom-up = **24–72 млн ₽**; preferred беру **24 млн ₽**.
- SOM bottom-up Y1 при capture 3% = **0,72 млн ₽**.
- SOM bottom-up Y3 при capture 10% = **2,4 млн ₽**.

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | н/д, для invest-case не нужен, фокус на РФ | — | — | top-down n/a |
| TAM (РФ) | 35 млн ₽ [T2] | 24 млн ₽ [T1/T2] | diff 1,46x, допустимо, bottom-up строже | **24 млн ₽** |
| SAM (РФ) | 21 млн ₽ [T2] | 24 млн ₽ [T1/T2] | diff 1,14x, в пределах нормы | **21 млн ₽** |
| SOM Y1 | 0,63 млн ₽ | 0,72 млн ₽ | diff 14% | **0,63 млн ₽** |
| SOM Y3 | 2,1 млн ₽ | 2,4 млн ₽ | diff 14% | **2,1 млн ₽** |

## 10 реальных buyers / target accounts для bottom-up
1. Ростелеком Контакт-центр [T2]
2. VOXYS [T2]
3. NEOVOX [T2]
4. Телеконтакт [T2]
5. MANGO OFFICE Contact Center [T2]
6. МТС Exolve / МТС Contact Center [T2]
7. S7 Airlines customer support [T2]
8. Аэрофлот customer support [T2]
9. Ostrovok / travel support [T2]
10. OneTwoTrip support [T2]

Это реальные компании, но **не доказанные текущие покупатели**. Это shortlist потенциальных target accounts; часть списка остаётся гипотезой для GTM, а не доказанным pipeline.

## Profit Gate (цель: EBITDA >= 500k ₽/мес)
### Сценарий 1, mid-market seat subscription
- ARR 1,2 млн ₽, gross margin 75%.
- Валовая прибыль на клиента в месяц: около **75 тыс. ₽**.
- Чтобы получить **500 тыс. ₽ EBITDA/мес**, нужно минимум **7 активных клиентов**, и это ещё без тяжёлых локальных sales/compliance costs.
- При preferred SOM Y1 **0,63 млн ₽** такой масштаб недостижим.

### Сценарий 2, enterprise account
- ARR 3,0 млн ₽, gross margin 70%.
- Валовая прибыль на клиента в месяц: около **175 тыс. ₽**.
- Нужно **минимум 3 enterprise клиента** одновременно.
- Для узкого сегмента bilingual contact-center в РФ и длинного цикла сделки это выглядит слишком оптимистично.

### Сценарий 3, high-touch integration
- ARR 6,0 млн ₽, gross margin 60%.
- Валовая прибыль на клиента в месяц: около **300 тыс. ₽**.
- Формально хватило бы **2 клиентов**, но такой сценарий требует enterprise integrations, security/legal review и длинного sales cycle; для standalone нового market container в РФ evidence недостаточен.

**Итог Profit Gate:** FAIL. Теоретически threshold достижим только в aggressive enterprise-сценарии с 2 крупными контрактами, но подтверждённого спроса на такой темп закрытия нет. Для инвестиционного standalone-case это недостаточно.

## Заключение
- **DEMAND = LOW**.
- **Profit Gate = FAIL**.
- Следовательно, кейс надо **REJECT** как самостоятельный рынок и считать supporting feature-layer внутри более широкого customer service operations / speech stack.

Sources: T1=2, T2=8, T3=3. Primary evidence basis: T2.