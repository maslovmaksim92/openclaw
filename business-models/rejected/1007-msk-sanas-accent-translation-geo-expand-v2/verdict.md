# 06-verdict

[GEO-EXPAND] 1007 MSK Sanas Accent Translation GEO Expand v2 — REJECTED: 22/100 | локальный спрос почти нулевой, fully-loaded CAC слишком высок, standalone economics не проходят фондовый порог.

## Кейс
1007-msk-sanas-accent-translation-geo-expand-v2

## Вердикт
**REJECTED**

## Почему
Кейс не проходит инвестиционный фильтр на уровне фонда.

### 1. Demand-side проблема
В `02-demand.md` локальный РФ-сигнал по category-level запросам почти нулевой. Есть только смежный спрос на contact-center AI и англоязычную поддержку, но не на самостоятельный budget line под accent translation.

### 2. Economics-side проблема
В `04-economics.md` standalone-модель не проходит key thresholds:
- **Blended fully-loaded CAC:** ~**1.78 млн ₽**
- **LTV:** ~**2.85 млн ₽**
- **LTV/CAC:** **1.60x**
- **Contribution Margin:** **38%**
- **CAC Payback:** **11.9 мес по CAC/MRR**, но **31.3 мес по gross profit**
- **Break-even:** **97-114 клиентов** в зависимости от fixed-cost base
- **При 50 клиентах EBITDA:** около **-3.6 млн ₽/мес**

### 3. Fund-level вывод
Это слишком узкий, sales-heavy и service-heavy продукт для standalone-инвестиции в РФ/СНГ. Экономика выглядит приемлемой только внутри более широкого voice/contact-center stack, где accent translation является feature, а не отдельной компанией.

## Что могло бы спасти кейс
Только один из двух сценариев:
1. продукт становится модулем внутри большого CCaaS / speech analytics бизнеса,
2. или появляется подтверждённый доступ к очень крупным международным BPO-контрактам вне РФ с ACV существенно выше 5-10 млн ₽ в год и лучшей валовой маржой.

В текущем standalone виде этого нет.
