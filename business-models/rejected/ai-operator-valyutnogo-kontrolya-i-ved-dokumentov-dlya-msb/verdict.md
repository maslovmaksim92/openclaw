---
stage: verdict
updated: 2026-05-11T04:10:00+03:00
verdict: REJECTED
---

[FINTECH] AI-оператор валютного контроля и ВЭД-документов для МСБ — REJECTED: 49/100 | EBITDA при 50 клиентах ≈ -4,26 млн ₽/мес, ниже profit gate 500 000 ₽/мес | LTV/CAC 6,9x не спасает тяжёлую fixed-cost базу regulated fintech delivery.

# 06-verdict

## Decision
**REJECTED**

## Why
Кейс прошёл demand-validation, но не проходит investment-grade unit economics.

### Ключевые причины
1. **Profit Gate FAIL**: при 50 клиентах EBITDA остаётся около **-4,26 млн ₽/мес**, тогда как порог требует достижимости **500k+ ₽/мес**.
2. **Fixed-cost base слишком тяжёлый** для regulated B2B fintech-модели с ARPU **55k ₽/мес**.
3. **Break-even только около 167 клиентов**, что слишком далеко для узкой ниши валютного контроля и ВЭД-документов.
4. Хотя **LTV/CAC = 6,3x** и **CAC payback = 9,1 месяца** выглядят приемлемо, это не спасает модель, потому что проблема в структуре команды, внедрения и managed exception handling.

## Investment view
Это выглядит не как software-scale opportunity, а как трудоёмкий hybrid service-heavy business с ограниченным потолком выручки и непропорционально высоким burn.

## What would need to change to reconsider
- ARPU должен быть заметно выше, ближе к enterprise/regional bank white-label.
- Либо продукт должен радикально снизить human exception workload и onboarding cost.
- Либо нужен другой buyer, например банки, крупные аутсорсеры или white-label канал, где 1 контракт даёт существенно больший ACV.

## Final note
Спрос есть, но в текущем wedge это **не инвестиционный SaaS / AI-native fundable case**.
