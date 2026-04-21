# Demand Validation — Conveyor

## Итог
**Решение на этапе Demand Validation: REJECTED (early reject).**

Причина: композитный спрос по РФ низкий, локальных Telegram/бот-каналов и заметного RU-category pull почти нет, а реалистичный SOM не поддерживает достижение **EBITDA ≥ 500 тыс. ₽/мес** ни в одном из проверенных сценариев монетизации. Основной вывод: продукт решает реальную боль у глобальных B2B SaaS-продавцов, но в РФ это слишком узкий sell-side trust/compliance workflow. [T1][T2]

## 1) Demand signals
- Internal multi-demand API по `security questionnaire automation`: **LOW**, score 0; Google Trends RU 0, HH 0, Yandex Suggest 2. Это указывает на почти отсутствующий прямой категорийный спрос в РФ. [T1/T2 mix]
- По `trust center`: **LOW**, score 15; HH 2 вакансии, Google Trends RU 1, Yandex Suggest 100. Есть слабый interest around the term, но не широкий buying wave. [T1/T2 mix]
- По `RFP automation`: **LOW**, score 0; HH 4 вакансии, Google Trends RU 0. Спрос в РФ выглядит эпизодическим и ближе к proposal tooling, чем к trust workflow. [T1/T2 mix]

## 2) Реальные конкуренты и цены
Ниже не только direct trust-center players, но и ближайшие substitutes, на которые реально уходит бюджет buyer-а.

| Игрок | Что продаёт | Цена | Комментарий |
|---|---|---:|---|
| Conveyor | trust center + questionnaire automation | **from $9,600/year** | Прямой референс по category pricing. [T2, official] |
| Loopio | RFP/RFI/security questionnaire automation | **from $20,000/year** | Верхний ориентир для зрелых bid/proposal teams. [T2, official] |
| 1up | questionnaire / answer automation | **$300/mo Starter, $900/mo Plus** | Более лёгкий AI-answering substitute. [T2, official] |
| UpGuard Trust Exchange | trust exchange / vendor trust workflows | **$600/mo billed annually** | Прайс на trust-side workflow заметно ниже enterprise suite. [T2, official] |
| DeepRFP | AI RFP software | **$75–125 per user/month** | Substitute со стороны proposal ops. [T2, official] |

**Вывод по цене:** willingness to pay существует, но чаще в глобальном англоязычном сегменте с enterprise-security questionnaires. Для РФ ближе реалистичный локальный price band — **0.8–1.5 млн ₽ ARR** на mid-market account или **30–100 тыс. ₽/мес** в low-touch сценарии. Это inference из публичных прайсов выше, при условном FX ~80 ₽/$ для сопоставимости. [T2 + inference]

## 3) WTP, proof of willingness to pay
- Conveyor публикует self-serve/entry pricing и указывает **Professional from $9,600/year**, то есть category уже monetized, а не pre-revenue experiment. [T2]
- Loopio держит **floor $20k/year**, что подтверждает готовность proposal/security teams платить заметные annual contracts за automation. [T2]
- 1up и DeepRFP показывают, что рынок accept-ит более дешёвые AI substitutes, но это одновременно ограничивает ceiling для локального SMB-пакета в РФ. [T2]
- В исходном intake для Conveyor зафиксировано **400+ customers** и enterprise-level logos; это дополнительное подтверждение, что боль коммерчески реальна, но уже на глобальном рынке. [T2]

**Итог по WTP:** WTP доказан глобально, но **локальный RU WTP слабее**, потому что buyer должен одновременно: 1) продавать B2B tech enterprise, 2) часто получать security questionnaires, 3) иметь англоязычный / международный revenue motion. Это резко сужает воронку. [T2]

## 4) Проверка Telegram и RU-ландшафта
- По ручному поиску и internal demand API, в РФ **не видно заметной ниши Telegram-ботов/сервисов**, которые специализированно автоматизируют security questionnaires, trust center access workflow или vendor trust responses. [T2/T3]
- В Telegram есть множество generic cybersecurity channels/bots, но они не являются substitute для Conveyor-class workflow automation. Это важно, потому что Telegram в РФ часто быстро проявляет локальный SMB-demand; здесь такого сигнала нет. [T3, supported by absence of T1/T2 demand signals]
- Локальный конкурентный ландшафт скорее состоит из кастомных процессов в Bitrix24/Notion/Confluence/Jira/Excel и точечных сервисных команд, а не из category-defining SaaS. [T3, спекуляция с оговоркой]

## 5) Market sizing

### Методология
- **Top-down:** взят global security software proxy **$87.5B** от Gartner и применена узкая доля **0.1%** на trust-center / questionnaire-automation niche. Затем использована российская прокси-ёмкость через локальный рынок ИБ-ПО **273.6 млрд ₽** и та же доля 0.1%. Это даёт нишевой TAM РФ **273.6 млн ₽**. [T1 Gartner via cited market figure, T2 MWS/CNews, inference]
- **Bottom-up:** принято **220** потенциальных buyers в РФ (enterprise-facing SaaS, cloud, cybersecurity, infra и digital-platform vendors, регулярно проходящие due diligence) × **35%** с реальной повторяющейся болью × **1.2 млн ₽ ARR** средний контракт. [T2 + inference, LOW CONFIDENCE]

### 10 реальных buyers для bottom-up sanity check
1. Yandex Cloud [T2]
2. VK Cloud / VK Tech [T2]
3. Selectel [T2]
4. Cloud.ru [T2]
5. Контур [T2]
6. МойСклад [T2]
7. МТС Web Services [T2]
8. BI.ZONE [T2]
9. Positive Technologies [T2]
10. Т1 Облако [T2]

### Таблица cross-check
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------:|----------:|----------------|-----------|
| TAM (мир) | **~7.0 млрд ₽** [T1/T2] | — | — | top-down |
| TAM (РФ) | **273.6 млн ₽** [T2 + inference] | **264.0 млн ₽** [T2 + inference] | diff=3.6%, близко | lower |
| SAM (РФ) | **164.2 млн ₽** [T2 + inference] | **92.4 млн ₽** [T2 + inference] | diff=1.8x, bottom-up строже из-за узкой воронки | **92.4 млн ₽** |
| SOM Y1 | **4.9 млн ₽** | **2.8 млн ₽** | diff=1.75x | **2.8 млн ₽** |
| SOM Y3 | **16.4 млн ₽** | **9.2 млн ₽** | diff=1.78x | **9.2 млн ₽** |

### Комментарии к sizing
- Расхождение top-down и bottom-up меньше 3x, значит sanity-check пройден. [T2]
- **SOM Y1 = 2.8 млн ₽** составляет около **3% от SAM**, то есть модель не overclaiming. [inference]
- При среднем цикле сделки 4–6 месяцев нужен pipeline сильно шире фактического SOM Y1; это дополнительно ухудшает исполнимость. [T3/T2]

## 6) Profit Gate: может ли компания выйти на EBITDA ≥ 500 тыс. ₽/мес?
Проверены все разумные сценарии.

### Сценарий A, low-touch SMB SaaS
- ARPA: **30 тыс. ₽/мес**
- Gross margin: **80%**
- Минимальный fixed opex: **~1.7 млн ₽/мес** (2 product/engineering, founder-sales, support/CS)
- Для EBITDA 500 тыс. ₽/мес нужна выручка: **(1.7 + 0.5) / 0.8 = 2.75 млн ₽/мес**
- Это **~92 платящих клиентов**.

**Вердикт:** не бьётся с низким спросом и слишком узкой категорией. [inference]

### Сценарий B, mid-market annual SaaS
- ARR на клиента: **1.2 млн ₽/год** (~100 тыс. ₽/мес)
- Gross margin: **80%**
- Для EBITDA 500 тыс. ₽/мес нужны те же **~2.75 млн ₽ MRR**, то есть **~28 клиентов**.

**Вердикт:** 28 клиентов требуют **33.6 млн ₽ ARR**, что в **3.7x выше preferred SOM Y3 = 9.2 млн ₽** и в 2x выше даже top-down SOM Y3. Gate fail. [inference]

### Сценарий C, enterprise + implementation
- Revenue per client: **~4.0 млн ₽/год** (лицензия + внедрение/кастомизация)
- Margin: **~65%** из-за сервисной нагрузки
- Opex: **~1.9 млн ₽/мес**
- Для EBITDA 500 тыс. ₽/мес нужна выручка: **(1.9 + 0.5) / 0.65 = 3.69 млн ₽/мес**
- Это **~11 enterprise accounts**.

**Вердикт:** при таком объёме выручки нужен ARR порядка **44 млн ₽**, что кратно выше реалистичного Y3 capture. Для РФ-нишевого продукта это малореально. [inference]

## 7) Вывод
- **Demand = LOW** по всем трём keyword angles. [T1/T2 mix]
- **WTP существует**, но главным образом в глобальном англоязычном сегменте. [T2]
- **RU Telegram / local SaaS signal почти отсутствует.** [T2/T3]
- **SAM и особенно SOM малы**, даже при умеренно оптимистичных предпосылках. [T2 + inference]
- **Profit Gate fail** во всех сценариях монетизации. [inference]

## Final demand verdict
**REJECTED at demand stage.** Для фонда это слишком узкий и слабо локализуемый рынок в РФ: category pain реальна, но локальная платёжная ёмкость и observable pull недостаточны.

### Источники
- Gartner security software market proxy, 2024. [T1]
- MWS/CNews, рынок ИБ-ПО в РФ 2024, **273.6 млрд ₽**. [T2]
- Conveyor pricing. [T2]
- Loopio pricing. [T2]
- 1up pricing. [T2]
- UpGuard Trust Exchange pricing. [T2]
- DeepRFP pricing. [T2]
- Internal multi-demand API (`security questionnaire automation`, `trust center`, `RFP automation`) with HH/Google Trends/Yandex suggest signals. [T1/T2 mix]

Sources: T1=2, T2=8, T3=2. Primary evidence basis: T2.