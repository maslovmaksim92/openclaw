[ECOMMERCE_ENABLEMENT] AI-карточки товаров и предметные фото для маркетплейсов — REJECTED: 36/100 | EBITDA при 50 клиентах = -5.27 млн ₽/мес | LTV/CAC=1.42x | Проблема: CAC уже как у сложного B2B, а ARPA и удержание остаются near-SMB.

# 06-verdict
sector: ECOMMERCE_ENABLEMENT

## Итог инвесткомитета
- **Вердикт:** **REJECTED**
- **Normalized score:** **36/100**
- **Статус по порогам:** <65 = reject, кейс не проходит в approve и переносится в `pipeline/rejected/`.
- **Ключевой вывод:** demand существует, но unit economics ломается на стыке низкого чека, высокой стоимости acquisition и слабых switching costs.

## Оценка
| # | Критерий | Вес | Raw (0-25) | Обоснование |
|---|----------|-----|------------|-------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 8 | «LTV/CAC = 1.42x», «CAC Payback = 16.6 мес», «Contribution Margin = 66.4%» из 04-economics.md. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 3 | «При 50 клиентах EBITDA = -5 265 000 ₽/мес», profit gate провален. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, WTP) | 25 | 18 | 02-demand.md подтверждает WTP, локальных конкурентов и SAM ~4 млрд ₽. |
| 4 | Moat | 25 | 8 | Категория коммодитизируется, switching costs низкие, distribution moat не доказан. |
| 5 | Execution Risk | 25 | 7 | Для low-ARPA продукта нужна тяжёлая команда и дорогой GTM, burn высокий. |
| 6 | GTM Realism | 25 | 10 | Каналы acquisition есть, но blended CAC 232K ₽ не бьётся с чеком 14K ₽ MRR. |

**Сумма raw:** 54/150  
**Normalized score = round((54 × 100) / 150) = 36/100**

## Почему REJECT
1. **Не проходит LTV/CAC.** База даёт только **1.42x** против investable порога **3:1**.
2. **Не проходит payback.** **16.6 мес** по выручке и **22.8 мес** по gross profit, что слишком долго для seller SaaS.
3. **Провален profit gate.** При **50 клиентах EBITDA = -5.27 млн ₽/мес**, то есть компания далека от 500K ₽/мес.
4. **Коммодитизация.** Продукт конкурирует не только с SaaS-аналогами, но и с дизайнерами, агентствами, PhotoRoom/Canva-классом и внутренними workflow селлера.

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| ARPA / MRR на клиента | 14 000 ₽/мес |
| COGS / клиент / мес | 3 800 ₽ |
| contribution_margin_rub_month | 9 300 ₽/клиент/мес |
| customer_ltv_rub | 329 032 ₽ |
| CAC | 232 218 ₽ |
| LTV/CAC | 1.42x |
| CAC Payback | 16.6 мес |
| GM% | 72.9% |
| fixed_costs_rub_month | 5 730 000 ₽ |
| company_ebitda_rub_month при 50 клиентах | -5 265 000 ₽/мес |
| Break-even | 617 клиентов / 8.63 млн ₽ выручки |
| startup_capital_to_bep_rub | >40 млн ₽ |

## Top-3 Risks
| Риск | Вероятность | Impact | Почему это top-3 |
|---|---|---|---|
| CAC inflation vs low ARPA | высокая | высокий | Привлечение seller-команд и агентств требует paid + sales assist, а чек слишком мал. |
| commodity retention | высокая | высокий | Клиенту легко уйти к аналогам, агентству или ручному дизайну. |
| burn before PMF | высокая | высокий | Даже аккуратный hire plan создаёт burn, который рынок с таким чеком не окупает. |

## Что должно было бы измениться для rerun
1. Поднять ACV минимум в 3-4 раза через enterprise/API/white-label motion.
2. Доказать бесплатный или почти бесплатный distribution moat через встроенность в маркетплейсы, ERP или seller-экосистему.
3. Показать churn существенно ниже 2%/мес, что для этой категории пока не подтверждено.
4. Сократить delivery/support слой, чтобы contribution на клиента был заметно выше 10K ₽.

## Финальный вывод
Кейс интересен как **small bootstrapped tool** или как feature inside larger seller platform, но **не как standalone investment-grade startup**. Спрос есть, однако в текущей конфигурации экономика не выдерживает фондовый фильтр.