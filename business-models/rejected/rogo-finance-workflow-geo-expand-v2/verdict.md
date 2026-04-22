---
stage: verdict
case: rogo-finance-workflow-geo-expand-v2
date: 2026-04-23
analyst: branch-models-lead
verdict: REJECTED
confidence: medium
investment_grade: false
sector: GEO-EXPAND
---

# 06-verdict — Investment Verdict

[GEO-EXPAND] Rogo Finance Workflow GEO Expand v2 — REJECTED: 56/100 | Реальная enterprise-боль есть, но в РФ buyer universe слишком узок, delivery слишком тяжёлый, и кейс не проходит Profit Gate.

## Итоговое решение
**REJECTED.**

Rogo-подобный finance workflow AI решает реальную боль для банков, УК, corpdev и advisory, но standalone geo-expand в РФ не проходит фондовый фильтр по экономике.

## Почему кейс отклонён
1. **Profit Gate не пройден.** В `04-economics.md` даже при **50 клиентах** модель остаётся ниже целевого порога: **EBITDA = -3,14 млн ₽/мес**.
2. **Break-even слишком далеко.** Contribution break-even требует около **89 клиентов**, а для `EBITDA > 500k ₽/мес` нужно **95 клиентов**.
3. **Это выше реалистичного buyer universe.** В `02-demand.md` preferred SAM по РФ составляет **144 млн ₽**, то есть рынок слишком узкий, чтобы уверенно набрать такую базу клиентов при enterprise motion.
4. **Delivery остаётся service-heavy.** Пилоты, security review, настройка workflow и analyst QA давят на валовую маржу и не дают превратить продукт в лёгкий SaaS.
5. **Даже сильный LTV/CAC не спасает кейс.** Формально `LTV/CAC = 5,3x`, но это не компенсирует структурно тяжёлую fixed-cost базу и длинный путь до окупаемости.

## Что в кейсе всё же сильное
- Есть подтверждённый adjacent demand по financial analysis, company intelligence и due diligence.
- ICP понятен: банки, УК, corpdev, advisory.
- В enterprise-сегменте willingness-to-pay реален, если продукт сокращает analyst-hours и ускоряет подготовку memo / deal materials.
- Глобально категория жизнеспособна, но локальный РФ-контур слишком узок для фондовой доходности.

## Ключевой инвестиционный вывод
Это **не investable РФ geo-expand кейс** в текущем виде. Чтобы пройти фильтр, модель должна была бы показать хотя бы одно из трёх:
- заметно более высокий ARPA,
- существенно более лёгкий delivery model,
- shared international scale вместо опоры только на РФ P&L.

Ни один из факторов пока не подтверждён достаточно убедительно.

## Риски, которые перевесили upside
- узкий локальный buyer universe;
- длинный enterprise sales cycle;
- высокий fully-loaded CAC;
- низкая для фонда gross margin;
- dependency на founder-led sales и service-heavy onboarding.

## Финальный статус для пайплайна
**Перевести кейс в `pipeline/rejected/`.**

## One-liner для инвесткомитета
**У Rogo есть реальная enterprise-боль, но в РФ это слишком узкий и дорогой workflow-бизнес: ценность есть, фондовой экономики нет.**

## Основание решения
- `00-brief.md`
- `02-demand.md`
- `04-economics.md`
