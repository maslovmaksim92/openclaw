# Celsus, AI-скрининг и ранняя диагностика для клиник и диагностических сетей v2
**Статус:** APPROVED WITH NOTES
**Итоговый балл:** 71/100
**Дата:** 2026-04-20
**Сектор:** HEALTHCARE
**Slug:** celsus-radiology-ai-screening-v2

---

## Этап 1 — Intake
Это rerun кейса `celsus-radiology-ai-screening`. Предыдущий verdict был **73/100** от **2026-04-19**. Повторный прогон запущен после обновления рубрики P4-P7: source tiering, fully-loaded CAC, hiring realism, Monte Carlo Lite, 6×25 scoring и moat framework.

## Этап 2 — Description / Evidence
Celsus — radiology AI-layer для клиник и диагностических сетей, встроенный в PACS / MIS / RIS workflow. Базовый тезис: клиники платят не за "AI ради AI", а за ускорение чтения исследований, снижение ошибки и стандартизацию screening-процесса. В evidence подтверждены category maturity, наличие reimbursement-like ценового якоря и зрелые локальные конкуренты.

## Этап 3 — Demand Validation
Demand API по категории вернул **LOW**, но кейс не ушёл в early reject, потому что enterprise WTP и category maturity подтверждены лучше, чем search-led сигналы. Источники по спросу: **T1=3, T2=8, T3=2**, weighted tier balance **2.08**, штраф к Market + Demand: **-2 балла**. Рабочий рынок по conservative reconciliation: **SAM 135-320 млн ₽/год**, **SOM Y1 18.7-23.4 млн ₽/год**.

## Этап 4 — Unit Economics
Ключевые метрики:
- ARPA: **185 000 ₽/мес**
- COGS: **46 000 ₽/мес**
- contribution_margin_rub_month: **139 000 ₽/мес**
- Gross Margin: **75.1%**
- Blended CAC: **686 000 ₽**
- customer_ltv_rub: **11 583 333 ₽**
- LTV/CAC: **16.9x**
- CAC Payback: **3.7 мес**
- fixed_costs_rub_month: **5 205 000 ₽/мес**
- Break-even: **38 клиентов**
- startup_capital_to_bep_rub: **39 784 626 ₽**

Вывод: economics инвестиционно сильная, но требует выдержать premium pricing и не размыть margin кастомными интеграциями.

## Этап 5 — Finance Risk + Critic
Monte Carlo Lite показывает неоднозначный профиль: **p10 EBITDA @M24 = -1.05 млн ₽/мес**, **p50 = 8.56 млн ₽/мес**, **p90 = 12.47 млн ₽/мес**. Главные fragility points: price compression, длинный pilot-to-paid cycle, кастомные PACS / MIS / RIS интеграции, regulatory burden и cash runway при длинном sales cycle.

## Этап 6 — Финальный вердикт
**APPROVED WITH NOTES, 71/100.**

### Score table
| # | Критерий | Вес | Raw (0-25) | Комментарий |
|---|----------|-----|------------|-------------|
| 1 | Unit Economics | 25 | 22 | LTV/CAC 16.9x, payback 3.7 мес, GM 75.1% |
| 2 | EBITDA Potential | 25 | 21 | 500К EBITDA достижимы примерно на 42 клиентах к 14 месяцу |
| 3 | Market + Demand | 25 | 15 | LOW search-demand, но WTP и category maturity подтверждены |
| 4 | Moat | 25 | 15 | compliance + integration + embedded workflow, но без сильного data flywheel |
| 5 | Execution Risk | 25 | 14 | высокая зависимость от pricing, integrations и regulated delivery |
| 6 | GTM Realism | 25 | 19 | repeatable enterprise motion и список реальных buyers присутствуют |

**Сумма raw:** 106/150  
**Normalized score:** **71/100**

### Investment one-liner
[HEALTHCARE] Celsus — APPROVED WITH NOTES: 71/100 | EBITDA base=8560К₽/мес через 24 мес | LTV/CAC=16,9x | Ключевое преимущество: глубокая интеграция в radiology workflow и RU procurement-ready контур | Главный риск: pricing pressure и длинный pilot-to-paid цикл.

### Top-3 risks
1. **Price compression**: сделки ниже 130K MRR быстро ломают economics.
2. **Integration drag**: кастомные PACS / MIS / RIS внедрения съедают roadmap и margin.
3. **Cash runway**: base M12 ещё отрицательный, а downside-сценарий остаётся живым даже на 24 месяцах.

### Что доказать для de-risking
1. Pilot-to-paid conversion **>=30%** на первых 8-10 пилотах.
2. Blended ARPA **>=130 000 ₽/мес** без системных скидок **>25%**.
3. Минимум 2 reference accounts с go-live cycle **<90 дней**.

### GTM named targets
МЕДСИ, Будь Здоров, Мать и дитя / MD Medical, СМ-Клиника, EMC, РЖД-Медицина, Скандинавия / АВА-ПЕТЕР, INVITRO, KDL, Ситилаб.

---

Источник артефакта: `/home/node/.openclaw/workspace/branch-models-lead/pipeline/approved/celsus-radiology-ai-screening-v2/06-verdict.md`
