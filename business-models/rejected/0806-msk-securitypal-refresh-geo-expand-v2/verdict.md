---
stage: verdict
case: 0806-msk-securitypal-refresh-geo-expand-v2
date: 2026-04-20
analyst: branch-models-lead
verdict: REJECTED
---

# 06-verdict

[GEO-EXPAND] 0806 MSK SecurityPal Refresh GEO Expand v2 — REJECTED: 0/100 | trust/security questionnaire pain реален, но LTV/CAC 0,77x и EBITDA остаётся отрицательной даже при 50 клиентах.

## Итог
**REJECTED**

## Почему
Кейс не проходит обязательный economics gate сразу по двум основаниям:

1. **LTV/CAC = 0,77x**, что **ниже 1:1**.
2. **Даже при 50 клиентах EBITDA остаётся отрицательной: -1,69 млн ₽/мес**.

## Ключевые цифры
- MRR на клиента: **180 000 ₽/мес**
- Gross Margin: **46,1%**
- Contribution Margin: **35,6%**
- Fully-loaded CAC: **3 853 143 ₽**
- LTV: **2 964 286 ₽**
- CAC Payback: **21,4 месяца**
- Break-even: **77 клиентов**

## Инвестиционная интерпретация
Рынок и pain реальные, но standalone-модель для локального запуска выглядит слишком service-heavy:
- acquisition дорогой и founder-dependent,
- renewal-risk выше нормального enterprise SaaS,
- fixed-cost база тяжёлая,
- free-entry trust center ослабляет pricing power.

Это делает кейс слабым именно как **самостоятельный fund-level инвестиционный актив**.

## Что могло бы изменить verdict
Только один из следующих сценариев:
1. продукт уходит в software-first с GM >70%;
2. blended CAC падает ниже ~900k ₽;
3. реальный ARPA стабильно >350k ₽/мес при churn <1,8% monthly;
4. кейс объединяется с более широким trust-workflow platform play, где shared GTM и platform economics лучше.

## Финальное решение для пайплайна
- Статус: **REJECTED**
- Действие: **перенести кейс в `pipeline/rejected/`**
