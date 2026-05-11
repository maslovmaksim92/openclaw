# 07-score-trajectory

## 2026-05-11 — P3 Demand Validation
- stage: P3-demand-validation
- analyst: branch-models-lead
- score_before: NEW
- score_after: PASS_WITH_RESERVATIONS
- trajectory: узкий спрос на AI-слой и voice-документацию в РФ пока слабый, но bundled-спрос на стоматологическую МИС, CRM, patient journey и compliance уже коммерческий; кейс стал investable только в upper-SMB и network positioning.
- key_deltas:
  - По demand API exact-demand по `стоматологическая мис`, `мис для стоматологии`, `егисз стоматология` и `голосовое заполнение медкарты` оказался низким.
  - Adjacent-demand по `crm для стоматологии` подтверждён как MEDIUM, что поддерживает go-to-market через понятный business outcome, а не через новый AI-category label.
  - Публичные цены 1С, БИТ.Стоматология, MNEMIX и TG-сервисов подтвердили willingness to pay и существование реального software budget.
  - Profit Gate провален в low-end single-clinic и compliance-only сценариях, но пройден в bundled upper-SMB, multi-clinic и network сценариях.
  - Итоговый риск сместился из вопроса «есть ли спрос вообще» в вопрос «сможет ли команда удержать высокий чек и правильный ICP».
- artifact: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/future-it-dent-ai-mis-dlya-stomatologiy/02-demand.md

## 2026-05-11 — P5 Unit Economics
- stage: P5-unit-economics
- analyst: branch-models-lead
- score_before: PASS_WITH_RESERVATIONS
- score_after: REJECT
- trajectory: кейс подтвердил buyer pain и willingness to pay, но сломался на unit economics, потому что regulated healthtech GTM, внедрение, compliance и required team делают fixed-cost базу слишком тяжёлой относительно achievable ARPU в стоматологиях.
- key_deltas:
  - Fully-loaded blended CAC посчитан на уровне **752,8 тыс. ₽**, что попадает в healthtech B2B benchmark, но подтверждает дороговизну acquisition и long-cycle sales motion.
  - Gross LTV получился около **2,72 млн ₽**, а **LTV/CAC = 3,61x**, то есть acquisition сам по себе не мёртвый, но запас прочности ограничен.
  - Contribution margin после realistic COGS и acquisition allocation составил лишь около **31,3%**, чего недостаточно для тяжёлой команды и compliance-нагрузки.
  - Fully-loaded FOT реалистичной команды вышел на **6,11 млн ₽/мес**, а общий fixed-cost base на **7,10 млн ₽/мес**.
  - Break-even требует около **192 клиентов**, а для **500k+ ₽ EBITDA/мес** нужно порядка **206 клиентов**.
  - Mandatory profit gate провален: при **50 клиентах** модель даёт около **-5,25 млн ₽ EBITDA/мес**, поэтому кейс не является investment-grade.
- artifact: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/future-it-dent-ai-mis-dlya-stomatologiy/04-economics.md