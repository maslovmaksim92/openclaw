---
stage: demand-validation
case: darrow-geo-expand-v2
date: 2026-04-21
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: REJECTED
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
Darrow, litigation intelligence и поиск массовых юридических претензий для plaintiff-side команд, litigation finance и смежных dispute workflows.

## Итог
**Статус: REJECTED.**

- Mandatory demand endpoint по ключам `litigation intelligence`, `судебная аналитика`, `мониторинг судебных дел`, `mass claims legal ai` в РФ вернул везде **LOW**. Наиболее близкие русскоязычные категории дают hh-proxy, но не показывают category pull именно под mass-claims / plaintiff intelligence. [T2: http://172.18.0.1:9001/multi-demand?keyword=litigation%20intelligence ; http://172.18.0.1:9001/multi-demand?keyword=%D1%81%D1%83%D0%B4%D0%B5%D0%B1%D0%BD%D0%B0%D1%8F%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA%D0%B0 ; http://172.18.0.1:9001/multi-demand?keyword=%D0%BC%D0%BE%D0%BD%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%BD%D0%B3%20%D1%81%D1%83%D0%B4%D0%B5%D0%B1%D0%BD%D1%8B%D1%85%20%D0%B4%D0%B5%D0%BB ; http://172.18.0.1:9001/multi-demand?keyword=mass%20claims%20legal%20ai]
- Глобальный market proof существует, но в РФ buyer/problem-fit хуже: локальный рынок больше про мониторинг дел, проверку контрагентов и defendant-side risk/compliance, чем про industrialized plaintiff-side class actions. Это ослабляет локальный wedge Darrow. [T2]
- WTP подтверждён только для смежных инструментов судебной аналитики и мониторинга, но не для high-ticket mass-claims discovery layer в РФ. [T2]
- Profit Gate не проходит ни в одном реалистичном локальном сценарии: self-serve seats, boutique subscription, contingency/rev-share, enterprise compliance pivot. Следовательно, выполняется правило раннего reject: **DEMAND=LOW + Profit Gate FAIL**. [T2]

## 1. Demand data

### Mandatory endpoint
- `litigation intelligence` → **LOW**, `demand_score=0`, `google_trends_ru=0`, `hh_ru=0`, `habr_articles=2`, `yandex_suggest=2`. [T2]
- `судебная аналитика` → **LOW**, `demand_score=22`, `google_trends_ru=1`, `hh_ru=174`, `habr_articles=2`, `yandex_suggest=100`. Это сигнал спроса на broader legal analytics, а не на Darrow-class plaintiff-intelligence. [T1/T2]
- `мониторинг судебных дел` → **LOW**, `demand_score=26`, `google_trends_ru=1`, `hh_ru=265`, `habr_articles=2`, `yandex_suggest=100`. Это сильнее для monitoring/compliance, но опять не для mass claims discovery. [T1/T2]
- `mass claims legal ai` → **LOW**, `demand_score=0`, `hh_ru=0`, `yandex_suggest=2`. [T2]

### Интерпретация
- В РФ есть спрос на судебный мониторинг и контрагентскую аналитику.
- Но это **adjacent demand**, не подтверждение покупательской категории `litigation intelligence for mass plaintiff claims`.
- Для Darrow это критично, потому что core ROI строится на систематическом поиске массовых оснований для исков, а не просто на удобном мониторинге судебных дел.

## 2. Реальные конкуренты с ценами

| Игрок | Что продаёт | Публичная цена | Что это значит |
|---|---|---|---|
| Docket Alarm | поиск docket'ов, court monitoring, alerts, analytics | **$99/мес** flat-fee; PAYG: **$4/document**, **$3/day alerts**, **$2/day docket tracking**, **$1/search** [T2: https://www.docketalarm.com/pricing] | глобальный рынок платит за litigation research, но starting price низкий и ближе к research tool, чем к Darrow-level platform |
| UniCourt | litigation data, analytics, docket research | **$49 / $149 / $299 в месяц** по self-serve планам [T2: https://unicourt.com/pricing] | существует платёжеспособный рынок court analytics, но price anchors умеренные |
| Casebook | проверка контрагентов, мониторинг судебных дел, арбитражная аналитика в РФ | **78 000 ₽/год за рабочее место**, более продвинутый контур **108 000 ₽/год за рабочее место** [T2: https://casebook.ru/] | локальный buyer уже платит за court monitoring, но по логике subscription-to-data, не success-fee plaintiff discovery |

### Вывод по ценовой вилке
- Подтверждённый ценовой коридор публичных аналогов находится примерно от **3,7 тыс. ₽/мес** эквивалента до **9 тыс. ₽/мес** и **78-108 тыс. ₽/год за место** в РФ, плюс usage-fees у Docket Alarm. [T1/T2, пересчёт по ЦБ РФ не требовался для reject-логики]
- Это доказывает willingness to pay за litigation data и monitoring, но не доказывает готовность российского рынка покупать отдельный дорогостоящий слой под массовые plaintiff claims. [T2]

## 3. Telegram bots / services в РФ
- Mandatory endpoint по всем релевантным ключам показывает `telegram subscribers = 0`. [T2]
- На российском рынке я не нашёл заметного Telegram-first продукта именно для litigation intelligence / поиска массовых претензий; в лучшем случае Telegram используется как канал уведомлений, а не как самостоятельный продуктовый wedge. [T2]
- Следовательно, Telegram не даёт дополнительного distribution proof для Darrow-подобного запуска в РФ. [T2]

## 4. WTP, willingness to pay

### Что подтверждено
1. **Платят за судебную аналитику и мониторинг.** Это видно по публичным тарифам Docket Alarm, UniCourt и Casebook. [T2]
2. **Платят за снижение ручного труда юристов и аналитиков.** hh-proxy по `судебная аналитика` и `мониторинг судебных дел` показывает заметный hiring, то есть компании уже тратят деньги на ручной labor в этих функциях. [T1/T2]
3. **Платят за risk/compliance и defendant-side visibility.** Российские инструменты типа Casebook продаются именно через мониторинг, проверку контрагентов и исковую нагрузку. [T2]

### Что НЕ подтверждено
1. **Не подтверждён локальный WTP за mass-claims discovery.** В РФ нет сильных публичных сигналов по litigation-finance-at-scale или plaintiff-side industrial discovery. [T2]
2. **Не подтверждён enterprise чек уровня Darrow.** Публичные локальные price anchors заметно ниже того, что нужно для fund-return economics. [T2]
3. **Не подтверждён короткий путь от insight к монетизации.** Даже если система находит паттерн претензий, дальше нужны юристы, процессуальный контур, funding и долгий time-to-cash. [T2]

### Вывод по WTP
**WTP есть для adjacent monitoring, но нет достаточного доказательства WTP для core Darrow use case в РФ.**

## 5. Market sizing

### Методика и оговорка
Секция строится как консервативная оценка рынка **в РФ именно для Darrow-подобного litigation intelligence слоя**, а не для всего legaltech. База доказательств в основном T2, поэтому расчёт нужно читать как рабочую инвестиционную оценку, а не как точную статистику.

### Top-down
- Top-down anchor: в РФ уже существует платный рынок судебного мониторинга/контрагентской аналитики, но Darrow адресует лишь узкий слой вокруг repeatable mass-claims discovery. В качестве proxy для addressable spend беру **примерно 1,2 млрд ₽** как узкий верхний слой litigation analytics / claims discovery в РФ, выведенный из наличия платных RU vendors и ограниченного числа реальных тяжёлых buyer'ов. [T2, inference]
- **TAM (РФ)** = **1,2 млрд ₽**. [T2]
- **SAM (РФ)** = TAM × 35% segment fit = **420 млн ₽**, где segment fit означает только buyer'ов с достаточным объёмом судебных данных и денежной мотивацией, чтобы покупать не monitoring, а intelligence layer. [T2, inference]
- **SOM Y1** = SAM × 2% = **8,4 млн ₽**. [T2, inference]
- **SOM Y3** = SAM × 7% = **29,4 млн ₽**. [T2, inference]

### Bottom-up
- **Total buyers** = **40**. Это консервативный список верхнего слоя: крупные dispute firms, банки, страховщики, debt/legal recovery игроки и несколько claims-heavy корпораций. [T2, inference]
- **% with need** = **50%**. Только половина из них реально имеет постоянную боль, подходящую под automated claims discovery, а не обычный court monitoring. [T2, inference]
- **ARR avg** = **12 млн ₽/год**. Это уже выше публичных seat-тарифов и требует enterprise justification; беру как upper-bound для локального Darrow-подобного пилота плюс аналитический контур. [T2, inference]
- **SAM_bottom_up** = 40 × 50% × 12 млн ₽ = **240 млн ₽**. [T2]
- **SOM_bottom_up Y1** = **6 млн ₽**. Это эквивалент одного ограниченного клиента или двух маленьких пилотов. [T2, inference]
- **SOM_bottom_up Y3** = **24 млн ₽**. Это 2 полноценных клиента или 4 ограниченных контура. [T2, inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | — | — | Для reject-решения не использую, потому что локальный buyer-fit важнее глобального рынка | — |
| TAM (РФ) | 1,2 млрд ₽ [T2] | 480 млн ₽ [T2] | diff=2,5x, допустимо; bottom-up уже режет рынок до реального buyer set | lower |
| SAM (РФ) | 420 млн ₽ [T2] | 240 млн ₽ [T2] | diff=1,75x, расхождение объясняется тем, что top-down включает потенциальный compliance-adjacent слой, который Darrow может не забрать | lower |
| SOM Y1 | 8,4 млн ₽ | 6,0 млн ₽ | diff=40%, но оба сценария слишком малы для fund-level outcome | **используем 6,0 млн ₽** |
| SOM Y3 | 29,4 млн ₽ | 24,0 млн ₽ | diff=22,5%, всё ещё недостаточно для сильного venture-scale кейса | **используем 24,0 млн ₽** |

### 10 реальных buyers для bottom-up sanity check
1. Сбербанк, судебные и претензионные контуры. [T2]
2. ВТБ. [T2]
3. Альфа-Банк. [T2]
4. Т-Банк. [T2]
5. Ингосстрах. [T2]
6. СОГАЗ. [T2]
7. АльфаСтрахование. [T2]
8. АСВ / recovery-related legal workflows. [T2]
9. Pravo Tech / Casebook-adjacent enterprise legal buyers как channel proxy. [T2]
10. Крупные dispute boutiques и plaintiff-side практики из верхнего сегмента рынка. [T2]

Sanity check: даже при цикле сделки 6-12 месяцев модель **SOM Y1 = 6 млн ₽** означает максимум 1 ограничённый клиент за год. Это слишком мало, чтобы собирать strong venture economics. [T2]

## 6. Profit Gate, проверка всех сценариев монетизации

Цель гейта: компания должна иметь реалистичный путь к **EBITDA ≥ 500 000 ₽/мес**.

### Сценарий A. Self-serve / seat-based litigation analytics
- Цена: **20-60 тыс. ₽/мес** за пользователя, что уже выше публичных RU тарифов. [T2, inference]
- Валовая прибыль на клиента после data/ops/support: ориентир **12-35 тыс. ₽/мес**. [T2, inference]
- Чтобы выйти на **500 тыс. ₽ EBITDA/мес** даже при очень lean fixed cost **1,5 млн ₽/мес**, нужно **60+ платящих мест** высокого качества.
- Для Darrow-class продукта в РФ это нереалистично, потому что рынок plaintiff intelligence узкий, а seat-based alternative already covered by cheaper tools. [T2]
- **Вердикт: FAIL.**

### Сценарий B. Boutique subscription для litigation firms
- Цена: **300-500 тыс. ₽/мес** на фирму. [T2, inference]
- GM: **60%**.
- Валовая прибыль на клиента: **180-300 тыс. ₽/мес**.
- Для EBITDA **500 тыс. ₽/мес** при fixed costs **2,0 млн ₽/мес** нужно **9-14 клиентов**.
- В РФ нет подтверждения, что найдётся столько plaintiff-heavy / disputes-heavy фирм с постоянной потребностью именно в automated mass-claims discovery. [T2]
- **Вердикт: FAIL.**

### Сценарий C. Contingency / revenue-share на найденных кейсах
- На бумаге upside высокий, но cash conversion длинный: discovery → юридическая упаковка → иск → процесс → взыскание. [T2]
- Для EBITDA-цели нужно либо много выигранных дел, либо доступ к litigation finance, а оба элемента в РФ слабо подтверждены. [T2]
- Working capital и legal execution risk слишком велики для раннего venture кейса. [T2]
- **Вердикт: FAIL.**

### Сценарий D. Enterprise pivot в compliance / defendant-side early-warning
- Это самый жизнеспособный локальный сценарий, но он уже сильно уходит от core Darrow thesis и конкурирует с Casebook-классом продуктов. [T2]
- Реалистичный чек: **150-350 тыс. ₽/мес**. [T2, inference]
- Для EBITDA-цели понадобятся **10-15+ клиентов**, а это означает уже другой продукт, другой GTM и сильную конкуренцию с локальными incumbents. [T2]
- **Вердикт: FAIL.**

### Общий вывод по Profit Gate
**Profit Gate FAIL.** Ни один реалистичный локальный сценарий не даёт убедимого пути к **500 тыс. ₽ EBITDA в месяц** без очень сильных допущений.

## 7. Почему reject именно сейчас
- Demand по core категории в РФ низкий.
- Adjacent demand есть, но он относится к monitoring/compliance, а не к Darrow-style mass claims discovery.
- Ценовые якоря рынка ниже, чем нужно для комфортной venture economics.
- Локальный рынок слишком узкий и медленный по time-to-cash.

## 8. Решение для пайплайна
**Решение: REJECTED на этапе P4 Demand Validation.**

Основание: выполняется правило **DEMAND=LOW и Profit Gate FAIL**.

## Источники
- [T2] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=litigation%20intelligence
- [T2] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=%D1%81%D1%83%D0%B4%D0%B5%D0%B1%D0%BD%D0%B0%D1%8F%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA%D0%B0
- [T2] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BC%D0%BE%D0%BD%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%BD%D0%B3%20%D1%81%D1%83%D0%B4%D0%B5%D0%B1%D0%BD%D1%8B%D1%85%20%D0%B4%D0%B5%D0%BB
- [T2] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=mass%20claims%20legal%20ai
- [T2] Docket Alarm pricing: https://www.docketalarm.com/pricing
- [T2] UniCourt pricing: https://unicourt.com/pricing
- [T2] Casebook homepage and pricing blocks: https://casebook.ru/

Sources: T1=2, T2=7, T3=0. Primary evidence basis: T2.
