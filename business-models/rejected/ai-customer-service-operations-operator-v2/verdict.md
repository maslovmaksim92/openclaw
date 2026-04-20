# 06-verdict

[B2B-OPS] AI Customer Service Operations Operator v2 — REJECTED: 52/100 | спрос и WTP подтверждены, но fully-loaded CAC, service-heavy delivery и слабая прибыльность не дают fund-grade экономики.

## Кейс
AI Customer Service Operations Operator

## Дата вердикта
2026-04-20, Europe/Moscow

## Итог
**REJECTED. Итоговый балл: 52/100.**

Кейс не проходит investment-fund фильтр после Program 5. Спрос и WTP есть, но экономика компании разваливается на fully-loaded CAC и service-heavy delivery. При base case `ARPA = 300 000 ₽/мес` и `COGS = 230 000 ₽/клиент/мес` contribution profit составляет всего `70 000 ₽/клиент/мес`, из-за чего бизнесу нужно примерно **83 клиента для EBITDA=0** и около **90 клиентов для EBITDA=500k/mo**. Даже при **50 клиентах EBITDA остаётся отрицательной: -2 247 000 ₽/мес**. Дополнительно `LTV/CAC = 1,51x`, что сильно ниже инвестиционного порога **3:1**.

## Почему reject
1. **Profit Gate FAIL**: компания не может достичь **+500k EBITDA/mo даже при 50 клиентах**.
2. **LTV/CAC = 1,51x**. Это не инвестиционное качество, даже если формально выше 1:1.
3. **Contribution margin = 23,3%**. Для фонда это слишком service-heavy и слишком слабо масштабируется.
4. **Требуемый капитал до break-even > 60 млн ₽**, а runway при стартовом капитале 40 млн ₽ около 9-11 месяцев.

## Score breakdown
| Критерий | Балл | Макс | Почему |
|---|---:|---:|---|
| Реальный спрос | 14 | 20 | Demand и WTP подтверждены публичными ценами, заменителями и adjacent market pull. |
| Unit economics / прибыль компании | 8 | 25 | `LTV/CAC = 1,51x`, `CM = 23,3%`, `83 клиента до EBITDA=0`, `50 клиентов всё ещё убыточны`. |
| Масштабируемость | 8 | 20 | Автоматизация есть, но delivery остаётся тяжёлым и headcount-dependent. |
| Конкурентное позиционирование | 6 | 15 | Есть buyer pain, но платформы helpdesk и AI-native vendors давят сверху. |
| Барьеры входа | 6 | 10 | Есть know-how по workflow tuning, но слабый структурный moat. |
| Качество данных | 10 | 10 | Demand, pricing, churn benchmark и hiring realism подтверждены источниками. |
| **Итого** | **52** | **100** | **Ниже инвестиционного порога.** |

## Delta vs previous run
- Previous score: **56/100**
- New score: **52/100**
- **Delta: -4**

Новый прогон жёстче за счёт fully-loaded CAC, hiring realism и проверки EBITDA при 50 клиентах. Именно эти допущения делают reject более убедительным, чем в предыдущем прогоне.

## Однострочный investment verdict
**Хороший painkiller, плохой фондовый актив: клиентский спрос есть, но капитализация value в компании слишком слабая.**