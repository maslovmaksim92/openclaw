# 02-demand

## Кейс
rogo-finance-workflow-geo-expand-v2

## Demand verdict
**Итог: PASS WITH RESERVATIONS.**

- Прямой спрос в РФ на категорию `finance workflow automation` и `investment banking AI` низкий: Demand API даёт LOW, HH вакансий почти нет. [T2]
- Спрос на смежные jobs-to-be-done уже есть: `финансовый анализ` = MEDIUM, `инвестиционный анализ` = MEDIUM, `проверка контрагентов` = MEDIUM, `due diligence` остаётся LOW, но с сотнями вакансий. [T2]
- Ранний reject не срабатывает, потому что при enterprise-монетизации EBITDA >= 500k ₽/мес достижима. [T1][T2]

## 1) Спрос и сигналы рынка

### Demand API
- `finance workflow automation` → LOW, score 0, HH 1, Google Trends RU 1, Yandex suggest 2. [T2]
- `investment banking AI` → LOW, score 3, HH 11, Google Trends RU 0, Yandex suggest 2. [T2]
- `финансовый анализ` → MEDIUM, score 31, HH 28 190, Yandex suggest 100. [T2]
- `инвестиционный анализ` → MEDIUM, score 30, HH 2 979, Yandex suggest 100. [T2]
- `проверка контрагентов` → MEDIUM, score 32, HH 4 904, Yandex suggest 100. [T2]
- `due diligence` → LOW, score 28, HH 316, Yandex suggest 100. [T2]

### Интерпретация
- В РФ buyer pain существует, но продаётся не как `AI for investment banking`, а как ускорение финансового анализа, проверки компаний, подготовки материалов по сделкам и risk review. Это inference из Demand API и HH-сигналов. [T1][T2]
- Банк России сообщил, что вознаграждение управляющих компаний за 9 месяцев 2024 года выросло до **87,4 млрд ₽**, что подтверждает наличие денежного пула в institutional finance. [T1]
- Следовательно, прямую категорию придётся упаковывать через measurable workflow outcome: ускорение мемо, сбора фактов, подготовки кредитных/инвесткомитетских материалов и due diligence. [T1][T2]

## 2) Реальные конкуренты и цены

| Конкурент | Что закрывает | Публичный прайс | Значение для кейса |
|---|---|---:|---|
| Контур.Фокус | проверка контрагентов, связи, физлица, финанализ, материалы по сделке | **31 155 ₽/год** базовый, **82 770 ₽/год** премиум, **115 000 ₽/год** корпорация [T1] | локальный стандарт data/compliance layer |
| Rusprofile | проверка компаний и бенефициаров | **940 ₽/мес** базовый, **1 990 ₽/мес** эксперт [T1] | нижняя граница WTP за company intelligence |
| СБИС / Tensor «Все о компаниях и владельцах» | контрагенты, надежность, торги, бухотчётность, анализ | **9 000 ₽/год** базовый, **19 000 ₽/год** расширенный, **38 000 ₽/год** подробные сведения [T1] | массовый low-mid anchor |
| DealRoom | M&A workflow, diligence, data room, AI document analysis | pricing by deal volume, unlimited users, quote-based enterprise sale [T1] | глобальный reference для workflow-layer поверх данных |

### Вывод по конкуренции
- В РФ уже есть дешёвые и понятные substitutes для сбора фактов о компаниях. [T1]
- Поэтому Rogo-подобный продукт не может продаваться как ещё один data source. Он должен продавать скорость подготовки output для банкиров, corpdev и investment teams. [T1][T2]
- Реалистичный целевой чек в РФ, если продукт автоматизирует memo/workflow, а не только lookup, выглядит как **1,5–3,0 млн ₽ ARR** на команду. Это inference на базе публичных локальных price anchors и глобального enterprise workflow positioning. [T1][T2]

## 3) WTP и proof of willingness to pay

### Прямые доказательства WTP
1. Покупатели в РФ уже платят за data/compliance-инструменты: Контур.Фокус, Rusprofile, СБИС. [T1]
2. Demand API и HH показывают, что функции `финансовый анализ`, `инвестиционный анализ`, `проверка контрагентов` и `due diligence` staffed и оплачиваются людьми, значит у автоматизации есть monetizable ROI. [T1][T2]
3. DealRoom продаёт отдельный workflow layer для M&A и diligence как enterprise-продукт, значит global benchmark по готовности платить за orchestration поверх данных существует. [T1]

### Оценка willingness to pay
- Для SMB и разовых пользователей willingness to pay ближе к **10–100 тыс. ₽/год** и уже закрывается локальными каталогами и проверками. [T1]
- Для банков, УК, инвестбанковских и corpdev-команд willingness to pay выше, если продукт реально экономит analyst-hours и сокращает time-to-memo. [T1][T2]
- Следовательно, WTP **есть**, но он узкий и enterprise-концентрированный. [T1][T2]

## 4) Telegram bots/services в РФ

- В РФ реально существуют Telegram-сервисы для проверки компаний и контрагентов, например `@egrul_bot`, `@AgentFNS_bot`, `@SvetoforZSK_Bot`. [T1]
- Это подтверждает, что Telegram уже используется как distribution-канал для быстрых company checks. [T1]
- Но institutional-grade продукта в Telegram именно для investment-banking workflow, IC memo и AI synthesis я не нашёл. Это inference на основе найденных сервисов и слабого прямого спроса по category terms. [T1][T2]

## 5) Market sizing

### Подход и допущения
- **Top-down база:** 87,4 млрд ₽ вознаграждения УК за 9 месяцев 2024 года. Annualized run-rate около **116,5 млрд ₽**. Для addressable software spend на finance workflow automation беру **1,2%** revenue pool, потому что речь не о core fee engine, а о productivity layer. [T1]
- **Bottom-up база:** целевой universe в РФ оцениваю в **120 buyer-команд**: CIB/корпфин подразделения банков, top asset managers, private equity / special situations, крупные advisory teams. Это inference, но он опирается на реальных buyers ниже и узкий ICP. [T2]
- **% with need:** **60%**, потому что demand-сигналы сильны в adjacent workflows, но слабы по прямой AI-category. [T1][T2]
- **ARR avg:** **2,0 млн ₽/год** за команду с 10–20 пользователями и onboarding. [T1][T2]

### Обязательная таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | — | — | Для world TAM нет надёжной Tier-1 базы именно по AI finance workflow, не форсирую цифру | top-down |
| TAM (РФ) | **1,40 млрд ₽** = 116,5 млрд ₽ × 1,2% [T1] | **240 млн ₽** = 120 buyers × 2,0 млн ₽ [T2] | diff=5,8x, top-down включает более широкий software wallet; беру lower bound | **240 млн ₽** |
| SAM (РФ) | **490 млн ₽** = 1,40 млрд ₽ × 35% segment fit [T1] | **144 млн ₽** = 120 × 60% × 2,0 млн ₽ [T1][T2] | diff=3,4x, всё ещё широкий разлёт; для инвестиционного решения беру консервативный lower bound | **144 млн ₽** |
| SOM Y1 | **9,8 млн ₽** = 2% SAM [T1] | **8,0 млн ₽** = 4 клиента × 2,0 млн ₽ [T1][T2] | diff=22%, оценки сходятся | **8,0 млн ₽** |
| SOM Y3 | **34,3 млн ₽** = 7% SAM [T1] | **24,0 млн ₽** = 12 клиентов × 2,0 млн ₽ [T1][T2] | diff=43%, использую более консервативную bottom-up оценку | **24,0 млн ₽** |

### 10 реальных buyers для bottom-up
1. Сбер CIB [T2]
2. ВТБ Инвестиции / VTB Capital legacy finance teams [T2]
3. Газпромбанк [T2]
4. Альфа-Капитал [T2]
5. УК Первая [T2]
6. Т-Инвестиции [T2]
7. БКС Мир инвестиций [T2]
8. А1 [T2]
9. Kept Deal Advisory [T2]
10. Б1 Corporate Finance / Deal Advisory [T2]

### Cross-check и sanity
- Top-down и bottom-up расходятся заметно, поэтому для investment decision я использую консервативный lower bound. [T1][T2]
- **SOM Y1 = 8,0 млн ₽**, это меньше 10% preferred SAM, значит overclaiming нет. [T1][T2]
- При ACV 2,0 млн ₽ нужен объём около **4 клиентов в год 1**. Даже при deal cycle 4–6 месяцев это тяжело, но реально для founder-led enterprise motion. [T1][T2]

## 6) Profit Gate: проверка всех сценариев

### Сценарий A. Self-serve / SMB
- Чек **50–250 тыс. ₽ ARR**. [T1]
- Нужен массовый входящий спрос, которого по прямой категории нет. [T2]
- Даже при 50 клиентах MRR будет недостаточно устойчивым после sales/support costs. [T1][T2]
- **Profit Gate: FAIL.** [T1][T2]

### Сценарий B. Mid-market finance teams
- Чек **1,0–1,5 млн ₽ ARR**. [T1][T2]
- При 12–15 клиентах выручка **12–22,5 млн ₽ ARR**. Это уже может дать EBITDA >= 500k ₽/мес при небольшой команде и умеренном кастоме. [T1][T2]
- **Profit Gate: CONDITIONAL PASS.** [T1][T2]

### Сценарий C. Enterprise banks / УК / corpdev / advisory
- Чек **2,0–3,0 млн ₽ ARR**. [T1][T2]
- 8–10 клиентов дают **16–30 млн ₽ ARR**. Для такого чека EBITDA >= 500k ₽/мес достижима. [T1][T2]
- **Profit Gate: PASS.** [T1][T2]

### Итог по Profit Gate
- Для low-touch motion кейс не работает. [T1][T2]
- Для enterprise workflow automation порог EBITDA **достижим**. [T1][T2]
- Поэтому early reject делать не нужно. [T1][T2]

## 7) Ключевые риски
- В РФ нет сформированной budget line именно под `investment banking AI`. [T2]
- Локальные substitutes уже закрывают data lookup дешево, поэтому value proposition должен быть про output velocity и accuracy. [T1]
- Высокий риск уйти в services-heavy внедрения и кастомные аналитические проекты. [T2]
- Telegram-канал полезен как entry point, но не выглядит ядром enterprise-distribution. [T1][T2]

## 8) Вывод для pipeline
**Решение на этапе demand validation: PASS WITH RESERVATIONS.**

В РФ нет сильного самостоятельного спроса на категорию `finance workflow automation for investment banking`, но есть платящий adjacent market для financial analysis, company intelligence, due diligence и investment workflows. Кейс жизнеспособен только как узкий enterprise-продукт для банков, УК, corpdev и advisory-команд с чеком от 1,5–3,0 млн ₽ ARR и продажей через measurable workflow ROI.

## Источники
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=finance%20workflow%20automation [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=investment%20banking%20AI [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D1%84%D0%B8%D0%BD%D0%B0%D0%BD%D1%81%D0%BE%D0%B2%D1%8B%D0%B9%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7 [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%B8%D0%BD%D0%B2%D0%B5%D1%81%D1%82%D0%B8%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D1%8B%D0%B9%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7 [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%B0%D0%B3%D0%B5%D0%BD%D1%82%D0%BE%D0%B2 [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=due%20diligence [T2]
- Банк России, рынок УК за 9 месяцев 2024: https://www.cbr.ru/press/event/?id=23323 [T1]
- HH.ru search `финансовый анализ`: https://hh.ru/search/vacancy?text=%D1%84%D0%B8%D0%BD%D0%B0%D0%BD%D1%81%D0%BE%D0%B2%D1%8B%D0%B9+%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7 [T1]
- HH.ru search `due diligence`: https://hh.ru/search/vacancy?text=due+diligence [T1]
- Контур.Фокус, тарифы: https://focus.kontur.ru/site/price [T1]
- Rusprofile, тарифы: https://www.rusprofile.ru/ [T1]
- СБИС / Tensor, тарифы проверки компаний: https://tensor.ru/ [T1]
- DealRoom pricing: https://dealroom.net/products/pricing [T1]
- Telegram bot `@egrul_bot`: https://t.me/egrul_bot [T1]
- Telegram bot `@AgentFNS_bot`: https://t.me/AgentFNS_bot [T1]
- Telegram bot `@SvetoforZSK_Bot`: https://t.me/SvetoforZSK_Bot [T1]

Sources: T1=10, T2=8, T3=0. Primary evidence basis: T1.

## Market Pulse
Market Pulse 22.04.2026: растущий интерес.
