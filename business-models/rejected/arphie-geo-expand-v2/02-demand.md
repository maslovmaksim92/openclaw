# Demand validation — Arphie geo expand (RU)

## Executive summary

**Итог:** в РФ есть подтверждённая боль вокруг тендеров, RFP и security questionnaires, но **core-demand именно на AI-автоматизацию DDQ / security questionnaires для enterprise B2B vendors остаётся низким**. По обязательному demand API: `RFP automation = LOW`, `security questionnaire automation = LOW`, `DDQ automation = LOW`, только широкий суррогат `тендерная автоматизация = MEDIUM` за счёт более общего рынка закупок и тендерного сопровождения [Internal demand API].

**Решение по этапу:** **EARLY REJECT**. Комбинация `DEMAND=LOW` + `Profit Gate FAIL` выполняется.

## Что продаёт Arphie

Arphie автоматизирует подготовку ответов на **RFP, DDQ и security questionnaires** для команд sales, presales и compliance. Это ближе к enterprise proposal management / trust management software, чем к массовым tender-monitoring ботам [T2].

## Competitor pricing и реальный reference price

Курс для пересчёта: **1 USD = 75.237 ₽** по данным ЦБ РФ на 21.04.2026 [T1].

| Конкурент | Прайс | В рублях | Комментарий |
|---|---:|---:|---|
| Loopio | от **$20,000/год** [T2] | от **1.50 млн ₽/год** | enterprise RFP response software, pricing public |
| Conveyor | от **$9,600/год** [T2] | от **722 тыс. ₽/год** | questionnaire automation + trust center |
| AutoRFP.ai | **$899/мес** Scale и **$1,299/мес** Accelerate [T2] | **67.6 тыс. ₽/мес** и **97.6 тыс. ₽/мес**; **811 тыс. ₽/год** и **1.17 млн ₽/год** | public SaaS pricing |

**Вывод по референсной цене:** международный ceiling для продукта класса Arphie выглядит как **0.72–1.50 млн ₽/год на клиента** [T2]. Для РФ разумно закладывать скидку 20–40% из-за локализации, импорта бюджетов в рубли и более длинного enterprise cycle, то есть **рабочий ARR для SAM/SOM = 0.5–0.7 млн ₽/год**, midpoint **0.6 млн ₽/год** [инференс на базе T2, помечено как осторожная оценка].

## Demand signals (RU)

### 1) Обязательный multi-demand API

- `RFP automation` → **LOW**; сигналы: HH 4, Habr 2, Yandex suggest 2 [Internal demand API]
- `security questionnaire automation` → **LOW**; HH 0, Habr 2, Yandex suggest 2 [Internal demand API]
- `DDQ automation` → **LOW**; HH 0, Habr 2, Yandex suggest 2 [Internal demand API]
- `тендерная автоматизация` → **MEDIUM**; HH 525, Yandex suggest 100 [Internal demand API]
- `опросники ИБ автоматизация` → **LOW**; HH 1 [Internal demand API]

**Интерпретация:** российский спрос виден в широком контуре тендеров и закупок, но не в узком use-case Arphie. Это важный negative signal: локальный рынок чаще платит за поиск тендеров, мониторинг, документооборот и сопровождение, а не за deep AI-automation ответов на buyer questionnaires.

### 2) Telegram bots/services в РФ

Найденные локальные сигналы:

1. **TRadar**: Telegram-first сервис под тендеры/лиды для агентств. Цены: **1,790 ₽/мес**, **5,090 ₽/3 мес**, **9,590 ₽/6 мес**, **17,990 ₽/год** [T2].
2. **LeadScanBot**: мониторинг Telegram-чатов, **10 ₽ за чат/день**, настройка под ключ **2,000 ₽** [T3, поддерживает тезис о низком локальном WTP].
3. **Росэлторг Telegram-бот**: существует как adjacent workflow для мониторинга закупок и тегов [T2 via search / product presence].

**Вывод:** Telegram-экосистема в РФ подтверждает наличие спроса на adjacent workflows, но на **низком чеке** и в логике tender discovery/monitoring, а не questionnaire-completion automation.

## WTP, willingness to pay

### Proof of willingness to pay

- На глобальном рынке покупатели уже платят **$9.6k–20k в год** за software этого класса, что подтверждает наличие категории и платёжеспособного use-case [T2].
- В РФ платёжеспособность подтверждается в смежном сегменте tender automation/monitoring, но с чеком **1.8k ₽/мес** у TRadar и микроподпиской у LeadScanBot [T2/T3].
- Следовательно, **WTP есть, но локально он доказан в соседнем, более дешёвом слое**. Для enterprise-tier pricing уровня Loopio/Conveyor в РФ прямых публичных доказательств почти нет.

### Оценка WTP

- **Low-end RU adjacent WTP:** 20–60 тыс. ₽/год [T2/T3]
- **Вероятный RU price for localized Arphie-class product:** 0.5–0.7 млн ₽/год [инференс из global comps T2]
- **High confidence на enterprise WTP в РФ отсутствует**, потому что прямых локальных сделок/кейсов по security questionnaire automation не найдено.

## Market sizing

### [LOW CONFIDENCE] Почему секция low confidence

Для узкого сегмента AI-автоматизации RFP/DDQ/security questionnaires в РФ нет хорошего публичного T1-рынка. Поэтому top-down строю от более широкого слоя коммерческого software stack, а bottom-up от числа вероятных покупателей и референсного ARPA. Диапазон использую консервативный, preferred = lower bound.

### Top-down

1. Российский рынок CRM в 2024 году оценивался примерно в **32.4 млрд ₽** [T2].
2. Для Arphie addressable share внутри CRM / RevOps / proposal stack оцениваю в **~2%**. Это очень узкий слой proposal management + questionnaire automation [инференс, anchored by low demand signals].
3. Тогда **TAM (РФ) ≈ 648 млн ₽** = 32.4 млрд × 2% [T2 + inference].
4. Для SAM беру только mid-market / enterprise B2B vendors с регулярными тендерами, infosec review и compliance questionnaires, то есть **~50% TAM**.
5. Тогда **SAM (РФ) ≈ 324 млн ₽**.
6. Реалистичный capture: **1% в Y1** и **4% в Y3**, потому что рынок объясняемый, cycle длинный, нужен trust layer и локализация.
7. Тогда **SOM Y1 ≈ 3.24 млн ₽**, **SOM Y3 ≈ 12.96 млн ₽**.

### Bottom-up

1. В реестре аккредитованных ИТ-компаний РФ фигурирует порядка **19 тыс. компаний** [T2, со ссылкой на Минцифры].
2. Для продукта Arphie релевантны не все, а только компании с enterprise sales motion, участием в закупках/RFP и security reviews. Консервативно беру **5%** как сегмент с повторяющейся болью. Это даёт **~950 потенциальных buyers** [T2 + Internal demand API + inference].
3. Средний контракт беру **0.6 млн ₽/год** как midpoint между Conveyor/AutoRFP/Loopio после РФ-дисконта [T2 + inference].
4. Получаем **SAM bottom-up ≈ 570 млн ₽** = 950 × 0.6 млн ₽.
5. Реалистичный capture: **0.5% Y1** и **2% Y3** из-за длинного цикла и узкой категории.
6. Тогда **SOM Y1 bottom-up ≈ 2.85 млн ₽**, **SOM Y3 bottom-up ≈ 11.4 млн ₽**.

### 10 реальных buyers для GTM / sanity check

1. VK Tech [T2]
2. Selectel [T2]
3. MTS Web Services [T2]
4. Positive Technologies [T1/T2]
5. BI.ZONE [T2]
6. Ростелеком-Солар [T2]
7. Контур [T2]
8. Arenadata [T2]
9. Yandex Cloud / Yandex B2B Tech [T2]
10. Группа Астра [T1/T2]

Это plausible buyers, потому что они продают enterprise software / infrastructure / security и регулярно проходят vendor questionnaires, presales и тендерные процедуры. Но это **не доказанные pipeline accounts Arphie в РФ**, а рабочий GTM-list.

### Reconciliation table

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | **$0.3–0.8B** для смежной категории proposal/RFP software [T3, speculative range] | — | мировой TAM не использую как основной | top-down range |
| TAM (РФ) | **648 млн ₽** [T2 + inference] | **~1.14 млрд ₽** если брать 19k × 10% × 0.6 млн ₽, но это слишком широко | bottom-up broad TAM завышает за счёт слишком широкого buyer pool | **648 млн ₽** |
| SAM (РФ) | **324 млн ₽** [T2 + inference] | **570 млн ₽** [T2 + inference] | расхождение 1.76x, допустимо; берем lower | **324 млн ₽** |
| SOM Y1 | **3.24 млн ₽** | **2.85 млн ₽** | расхождение 1.14x | **2.85 млн ₽** |
| SOM Y3 | **12.96 млн ₽** | **11.4 млн ₽** | расхождение 1.14x | **11.4 млн ₽** |

**Sanity checks:**
- Расхождение top-down vs bottom-up < 3x, ок.
- SOM Y1 < 10% SAM, ок.
- Даже при avg deal cycle 6–9 месяцев закрытие enough logos в Y1 выглядит тяжёлым: на выручку 2.85–3.24 млн ₽ нужно 4–6 сделок по 0.5–0.7 млн ₽, а рынок ещё требует category education.

## Profit Gate (EBITDA >= 500k ₽/мес)

Целевой gate: **EBITDA не ниже 500k ₽/мес**, то есть **6.0 млн ₽ EBITDA/год**.

Проверяю все базовые monetization scenarios.

### Сценарий A: low-ticket self-serve
- Цена: **180k ₽/год**
- Для 6 млн ₽ EBITDA/год даже при 70% EBITDA margin нужно **~48 клиентов**.
- Для узкого и low-demand сегмента в РФ это нереалистично.
- **FAIL**.

### Сценарий B: mid-market SaaS
- Цена: **600k ₽/год**
- При зрелой марже 35% нужно **~29 клиентов** для 6 млн ₽ EBITDA/год.
- Это сильно выше realistic SOM Y1 и выше разумного new-category capture.
- **FAIL**.

### Сценарий C: enterprise high-touch
- Цена: **1.2 млн ₽/год**
- При 25% EBITDA margin после внедрения, кастомизации, локализации и enterprise sales нужно **~20 клиентов**.
- Для РФ по такой узкой категории и текущим demand signals это тоже не бьётся.
- **FAIL**.

### Сценарий D: services + software hybrid
- Можно поднять чек за счёт managed response services / tender desk.
- Но тогда компания уходит в service-heavy модель с меньшей масштабируемостью, а не в software multiple. EBITDA может появиться точечно, но это уже другой бизнес.
- **FAIL для software thesis**.

**Вывод по Profit Gate:** при реалистичных сценариях **достигнуть 500k ₽ EBITDA/мес не получается**. Даже если выручка Y3 дотянется до 11–13 млн ₽, это всё ещё не гарантирует 6 млн ₽ EBITDA/год после sales, success, внедрения и локализации.

## Risks

1. **Category gap:** локальный рынок понимает тендерный мониторинг, но плохо демонстрирует спрос на questionnaire automation.
2. **Long sales cycle:** security/compliance workflows живут в enterprise procurement и доверии.
3. **Localization burden:** русский язык, шаблоны документов, legal/compliance context, интеграции.
4. **Adjacency pressure:** низкочековые local bots и tender-services оттягивают бюджет и формируют ожидание дешёвого решения.

## Verdict for P4

- **Demand:** LOW
- **WTP:** mixed, с подтверждением скорее в adjacent low-ticket сегменте
- **TAM/SAM/SOM:** есть, но узкие и low-confidence
- **Profit Gate:** FAIL
- **Decision:** **REJECTED / move to pipeline/rejected/**

Sources: T1=2, T2=9, T3=2. Primary evidence basis: T2.

## Source notes

- [T1] ЦБ РФ, daily_json.js, курс USD/RUB.
- [T1] HH.ru в этой работе использован как разрешённый tier-класс через internal demand endpoint.
- [T2] Loopio pricing: https://loopio.com/pricing/
- [T2] Conveyor pricing: https://www.conveyor.com/pricing
- [T2] AutoRFP.ai pricing: https://autorfp.ai/pricing
- [T2] TRadar pricing: https://www.tradar.me/
- [T2] TASS/Минцифры о количестве аккредитованных ИТ-компаний: https://tass.ru/ekonomika/23336595
- [T2] CNews / CRM market in Russia 2024: https://www.cnews.ru/reviews/crm_2024/articles/rynok_crm_v_rossii_vyros
- [T3] LeadScanBot pricing: https://leadscanbot.ru/czeny/
- [Internal demand API] http://172.18.0.1:9001/multi-demand?keyword=...
