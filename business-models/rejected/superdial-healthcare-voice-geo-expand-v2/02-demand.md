# 02-demand

## Итог
- **Demand verdict:** LOW
- **Profit Gate verdict:** FAIL
- **Решение этапа:** EARLY REJECT, так как спрос в РФ слабый, а сценарий достижения EBITDA >= 500 000 ₽/мес для отдельной компании по этой нише не подтверждается.

## 1) Demand signals
- По обязательному запросу `multi-demand` для ключа `healthcare voice automation revenue cycle payer calls клиники страховщики телефонные звонки` получено: `composite_demand=LOW`, `demand_score=0`, `hh_ru=0`, `google_trends_ru=0`, `habr_articles=2`, `yandex_suggest=2`. Это указывает на почти нулевой явный pull в РФ по узкому wedge payer-call / revenue-cycle voice automation [T1, internal pull from mandated endpoint].
- В РФ есть спрос на более широкую автоматизацию клиник и регистратуры, но он идёт через МИС, онлайн-запись, телефонию и напоминания, а не через отдельный budget line для AI-автоматизации звонков клиники страховщику [T2]. Medesk продвигает телефонию, онлайн-запись, SMS/email-напоминания и телемедицину как встроенные функции клинической платформы, то есть рынок чаще покупает bundled workflow, а не stand-alone payer-calling AI.

## 2) Реальные конкуренты и цены

| Конкурент | Что продаёт | Публичная цена | Вывод для кейса |
|---|---|---:|---|
| Retell AI | Voice AI platform, incl. HIPAA/BAA enterprise options | $0.07-$0.31/мин + $8/concurrency/мес + add-ons [T1] | Глобальный infra/player, но не локальный vertical winner в РФ; pricing usage-based, не enterprise ACV by default |
| Synthflow | Voice AI platform | обычно $0.15-$0.24/мин, voice engine в калькуляторе $0.09/мин, concurrency $20/unit/мес, white-label $2 000/мес [T1] | Ещё один horizontal stack, подтверждает commoditization voice layer |
| Bland AI | Flat per-minute voice AI | Start $0.14/мин; Build $0.12/мин + $299/мес; Scale $0.11/мин + $499/мес [T1] | Цена ядра рынка уже прозрачна и давит margin на local reseller / operator model |
| Medesk | МИС для частных клиник, включая телефонию/онлайн-запись/напоминания | бесплатный план до 50 приёмов/мес, далее платный тариф для растущей клиники [T1] | В РФ клиника часто выбирает bundled clinic OS вместо отдельного payer-call AI продукта |

**Вывод по конкурентам:** цена voice-automation слоя уже видна и достаточно низка у глобальных платформ [T1], а в РФ customer relationship и регистратура закрываются через МИС/телефонию [T1/T2]. Это снижает шанс, что узкий payer-call wedge станет самостоятельной большой категорией.

## 3) Проверка Telegram-ботов/сервисов в РФ
- Проверка показала, что в РФ уже присутствуют близкие substitutes через Telegram и мессенджер-автоматизацию, но в основном для записи пациента и коммуникации, а не для payer calls. В обзоре Medesk по рынку МИС упомянут **BOTMED** на базе Telegram у Medidea и наличие **WhatsApp/Telegram-ботов** у «Клиника Онлайн» [T2/T3].
- У Altegio есть AI Beauty Bot с поддержкой Telegram, но это adjacent beauty/wellness, а не healthcare revenue cycle [T2].
- Значит, Telegram-канал в РФ существует, но подтверждает скорее commoditized patient-facing automation, чем высокий спрос на insurer-calling AI [T2].

## 4) WTP, willingness to pay
- Public pricing у voice vendors указывает, что базовая стоимость самого voice/LLM/telephony слоя находится примерно в диапазоне **$0.07-$0.31/мин** или **$0.11-$0.14/мин + platform fee $299-$499/мес** [T1]. Следовательно, покупатель видит core engine как инфраструктуру, а не как стратегический system-of-record.
- Medesk как bundled clinic software продаёт entry-level ценность очень дёшево, начиная с бесплатного плана для малого объёма [T1]. Это давит на локальный WTP за отдельный stand-alone продукт для регистратуры/коммуникаций.
- **WTP proof слабый:** есть готовность платить за bundled clinic stack, телефонию и patient communication [T1/T2], но нет видимого публичного evidence, что российские клиники массово готовы выделять отдельный бюджет на AI-звонки страховщику / denial follow-up [T1 internal pull + T2 market reading].
- Поэтому для этого кейса WTP оцениваю как **слабый-средний на уровне feature spend, но не company-grade platform spend** [Inference based on T1/T2].

## 5) Market sizing

### Методика
- **Top-down:** от объёма коммерческой медицины в РФ.
- **Bottom-up:** от числа частных медицинских организаций и реалистичного числа buyers, которым действительно нужен insurer-facing / heavy-call workflow.

### Допущения
- Объём рынка частной медицины РФ в 2024 году: **>2 трлн ₽** по Kept, пересказ Vademecum [T2].
- Число частных медицинских организаций в РФ: **66 031** в 2024 году, пересказ RBC Marketing со ссылкой на исследование SYNOPSIS [T2].
- Для узкого voice automation wedge addressable share беру **0.5%** от коммерческого private healthcare spend как верхнюю границу category spend на коммуникационную automation прослойку; это **аналитическое допущение**, а не прямой observed spend [спекуляция, anchored by T1 competitor pricing + T2 market size].
- Доля реально подходящего сегмента (крупные/сетевые клиники, диагностические сети, клиники с DMS/страховым потоком, BPO revenue-cycle подрядчики): **15%** TAM [спекуляция].
- Реалистичный capture: **2% в Y1, 8% в Y3** [спекуляция, но в пределах sanity для B2B workflow software].
- Bottom-up средний контракт: **600 000 ₽/год** (50 000 ₽/мес) на account, исходя из того, что российский buyer чаще покупает коммуникационный слой как feature-bundle, а не как дорогой enterprise platform; это существенно ниже уровней, нужных для фонда-масштаба [Inference from T1 pricing].

### Таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | — | — | Для этого кейса не использую: вопрос не в глобальном voice AI, а в узком РФ wedge | — |
| TAM (РФ) | 10.0 млрд ₽ = 2.0 трлн ₽ × 0.5% [T2+T1/spec] | — | Bottom-up считаю сразу с сегмента buyers | top-down |
| SAM (РФ) | 1.5 млрд ₽ = 10.0 млрд ₽ × 15% [spec] | 1.19 млрд ₽ = 66 031 × 3% need × 600 000 ₽ ARR [T2+T1/spec] | diff ~26%; приемлемо, т.к. обе оценки описывают очень узкий enterprise-like subsegment | **1.19 млрд ₽** |
| SOM Y1 | 30 млн ₽ = 1.5 млрд ₽ × 2% | 23.8 млн ₽ = 1.19 млрд ₽ × 2% | diff ~26% | **23.8 млн ₽** |
| SOM Y3 | 120 млн ₽ = 1.5 млрд ₽ × 8% | 95.1 млн ₽ = 1.19 млрд ₽ × 8% | diff ~26% | **95.1 млн ₽** |

### 10 реальных buyers для bottom-up sanity check
1. ГК «Медси» [T2]
2. «Мать и дитя» / MD Medical [T2]
3. EMC [T2]
4. «СМ-Клиника» [T2]
5. «Будь Здоров» [T2]
6. «Медскан» [T2]
7. INVITRO [T2]
8. KDL [T2]
9. СОГАЗ ДМС / связанные медсервисы [T2]
10. РЕСО-Гарантия ДМС / связанные медсервисы [T2]

Это не доказательство покупки, а список реальных ICP/accounts для GTM sanity check [T2 + inference].

### Интерпретация sizing
- Даже при благожелательных допущениях получаем **SAM около 1.2-1.5 млрд ₽**, а **SOM Y1 около 24-30 млн ₽**. Для фонда это слишком узкий стартовый рынок, если core wedge не расширяется в полноценный healthcare ops platform.
- Поскольку сам mandatory demand pull в РФ равен LOW [T1], даже эта оценка выглядит как верхняя граница, а не base case.

## 6) Profit Gate: EBITDA >= 500 000 ₽/мес
Проверил все базовые сценарии monetization.

### Сценарий A. Pure software / clinic subscription
- Цена: 30-50 тыс. ₽/мес [Inference from T1 substitutes].
- Чтобы получить EBITDA 500 тыс. ₽/мес, при gross margin 80% и sales/support/G&A минимум 400-600 тыс. ₽/мес нужно примерно **25-35 платящих клиник**. Для такого узкого продукта это тяжело при demand LOW и длинном внедрении.
- **Вердикт:** FAIL.

### Сценарий B. Managed service для звонков/denial follow-up
- Цена: 70-120 тыс. ₽/мес за account [Inference].
- При gross margin 40-55% из-за QA, дообучения, операторского fallback и интеграций нужно порядка **12-18 клиентов**, чтобы стабильно выйти на EBITDA 500 тыс. ₽/мес.
- В РФ не найдено достаточного сигнала, что столько buyers готовы покупать именно этот narrow service line [T1/T2].
- **Вердикт:** FAIL.

### Сценарий C. Enterprise custom для сетей/страховых/BPO
- Цена: 150-300 тыс. ₽/мес возможна только у редких сетевых игроков [спекуляция].
- Но sales cycle, security/compliance, интеграции с МИС/телефонией/страховыми workflow и кастомизация съедают margin и замедляют ramp. 3-5 enterprise контрактов могли бы дать выручку, но не дают надёжного доказанного пути к EBITDA 500 тыс. ₽/мес на ранней стадии в РФ.
- **Вердикт:** FAIL.

### Общий вывод по Profit Gate
- Во **всех** разумных сценариях путь к **EBITDA >= 500 000 ₽/мес** есть только при оптимистичных допущениях о количестве клиентов и скорости продаж, которые не подтверждаются спросом [T1/T2].
- Следовательно, **Profit Gate = FAIL**.

## 7) Почему reject сейчас
1. Узкий спрос по обязательному demand pull: LOW [T1].
2. В РФ рынок покупает bundled clinic software / коммуникации, а не отдельный insurer-calling AI wedge [T1/T2].
3. Конкурентный voice layer уже commoditized и имеет публичный usage pricing [T1].
4. Profit Gate не проходит ни в одном основном monetization scenario.

## Источники
- Retell pricing: https://www.retellai.com/pricing [T1]
- Synthflow pricing: https://synthflow.ai/pricing [T1]
- Bland pricing: https://www.bland.ai/pricing [T1]
- Medesk pricing: https://www.medesk.ru/prices/ [T1]
- Medesk main product / telephony: https://www.medesk.ru/ , https://www.medesk.ru/telephony/ [T1]
- RBC Marketing: https://marketing.rbc.ru/articles/16251/ [T2]
- Vademecum on Kept private healthcare market: https://vademec.ru/news/2025/12/02/analitiki-za-pyat-let-rynok-chastnoy-meditsiny-v-rossii-vyros-na-76/ [T2]
- Kommersant on Rusprofile private medical companies: https://www.kommersant.ru/doc/8381085 [T2]
- Medesk review mentioning BOTMED / Telegram bots in clinic software market: https://www.medesk.ru/blog/medmis-obzor/ [T2/T3]
- Altegio AI Beauty Bot: https://alteg.io/ru/support/knowledge-base/altegio-%D0%B8-ai-beauty-bot/ [T2]

Sources: T1=6, T2=4, T3=1. Primary evidence basis: T1.
