---
stage: score-trajectory
updated: 2026-05-11T09:04:00+03:00
---

# 07-score-trajectory

## 2026-05-11 — Program 5 / Unit Economics

- Статус до шага: `02-demand.md` готов, `04-economics.md` отсутствовал.
- Действие: файл траектории создан заново как полный блок для шага Program 5.
- Что изменилось:
  - добавлен полный расчёт unit economics,
  - зафиксирован fully-loaded CAC вместо media-only CAC,
  - добавлены churn benchmark, LTV, CAC payback, contribution margin,
  - добавлены team/FOT, hiring realism, fixed costs, burn и break-even.
- Результат:
  - demand verdict остаётся отрицательным,
  - economics verdict: **FAIL**,
  - итоговый статус кейса: **REJECTED**.
- Ключевые метрики:
  - ARPA: **250 000 ₽/мес**
  - Contribution Margin: **28%**
  - Fully-loaded CAC: **1 276 667 ₽**
  - Churn: **6.0%/мес**
  - LTV: **1 166 667 ₽**
  - LTV/CAC: **0.91x**
  - CAC Payback: **18.2 мес**
  - Break-even: **~98 клиентов**
  - EBITDA @ 50 клиентов: **-3.30 млн ₽/мес**
- Решение по траектории score:
  - кейс не поднялся до investable,
  - после economics-check траектория ухудшилась с `demand FAIL` до `hard reject по economics + demand`.
