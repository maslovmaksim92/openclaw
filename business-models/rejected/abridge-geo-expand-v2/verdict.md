[HEALTHCARE] Abridge GEO Expand v2 — REJECTED: 64/100 | EBITDA base=718К₽/мес через 12 мес | LTV/CAC=22,2x | Ключевое преимущество: enterprise-on-prem workflow для крупных клиник | Главный риск: прямой спрос в РФ остаётся LOW.

# Abridge GEO Expand v2 — полный вердикт

sector: HEALTHCARE
status: REJECTED
score: 64/100
date: 2026-04-22

## Stage 1. Intake
- Источник: `2026-04-19-resurrect-abridge-geo-expand.md`
- Тип сигнала: resurrect / rerun.
- Исходная гипотеза: ambient clinical documentation как enterprise healthcare workflow layer для крупных клиник и медсетей.
- Почему кейс был переоткрыт: после обновления аналитической системы нужно было заново проверить спрос, economics, moat и GTM в РФ.

## Stage 2. Validation / Demand
- Mandatory endpoint по релевантным ключам дал **LOW**: `ambient clinical documentation = 0`, `медицинский речевой ассистент = 3`, `автоматизация протокола приема врача = 0`.
- При этом рынок боли существует: в РФ **749 885 врачей**, **23,1 тыс.** амбулаторно-поликлинических организаций, а локальные substitutes уже есть, включая Voice2Med, Aiston и «Звёздочку».
- Итог: self-serve сценарий для РФ слабый, но enterprise/on-prem wedge у крупных сетей реален.
- Sources tier balance: `T1=2, T2=16, T3=0`, weighted `2.11`, штраф к Market+Demand = `-2`.

## Stage 3. Economics
- recurring check на клиента: **1 800 000 ₽/мес**.
- COGS на клиента: **650 000 ₽/мес**.
- Gross profit: **1 150 000 ₽/мес**.
- Contribution profit: **1 000 000 ₽/мес**.
- Gross Margin: **63,9%**.
- customer_ltv_rub: **62 748 000 ₽**.
- CAC blended: **2 823 000 ₽**.
- LTV/CAC: **22,2x**.
- Adjusted stress LTV/CAC: **3,1x**.
- Practical CAC payback: **9-12 месяцев**.
- Break-even: **5-6 активных клиентов**.
- startup_capital_to_bep_rub: **29 159 268 ₽**.

## Stage 4. Finance / PnL / Risk
- Base-case `company_ebitda_rub_month` выходит в плюс к **M12 = 717 999 ₽/мес**.
- Optimistic case: break-even уже в **M7**, cumulative cash need около **15,1 млн ₽**.
- Pessimistic case: break-even не достигается за 12 месяцев.
- Sensitivity: `CAC x2 => EBITDA @M12 = -646 584 ₽`, `Price -30% => -2 260 640 ₽`.
- Monte Carlo Lite: `p10 EBITDA @M24 = -1 236 081 ₽`, `p50 = 5 020 479 ₽`, `p90 = 9 482 960 ₽`.
- Вывод: economics живая, но очень хрупкая к price compression, CAC inflation и deployment complexity.

## Stage 5. Critic scorecard

| # | Критерий | Raw |
|---|---|---:|
| 1 | Unit Economics | 20 |
| 2 | EBITDA Potential | 18 |
| 3 | Market + Demand | 11 |
| 4 | Moat | 13 |
| 5 | Execution Risk | 15 |
| 6 | GTM Realism | 19 |

**Sum raw = 96/150, normalized = 64/100.**

### 7-factor Moat
- Network effects: 0/3
- Switching costs: 2/3
- Scale economies: 2/3
- Proprietary data / model advantage: 1/3
- Regulatory moat: 2/3
- Brand / distribution: 1/3
- Embedded workflow: 3/3
- Итого: **11/21 => 13/25**

## Stage 6. Final verdict
**REJECTED.**

Почему:
1. Спрос в РФ остаётся ранним и напрямую не подтверждён, несмотря на наличие боли и substitutes.
2. Moat средний: интеграции и комплаенс создают барьер, но те же барьеры доступны локальным игрокам.
3. GTM enterprise-only, дорогой и зависимый от МИС-партнёров и локального deployment.
4. Economics достаточна для pilot-scale бизнеса, но не даёт investment-grade margin of safety для fund-return profile.

## Что должно измениться для пересмотра
- 2+ российских paid pilots в крупных частных медсетях.
- Подтверждённый on-prem blueprint под 152-ФЗ / 323-ФЗ.
- Edit rate врача < 15% по нескольким специальностям.
- Партнёрский канал через МИС, снижающий sales cycle до 6-8 месяцев.
- CAC ≤ 2,3 млн ₽ при recurring check ≥ 2,1 млн ₽/мес.

## GitHub summary
Кейс отклонён не потому, что экономика плохая, а потому что рынок и moat в РФ пока недостаточно доказаны. Это хороший кандидат для watchlist, но не для текущего approve.
