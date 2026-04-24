---
stage: verdict
case: supio-geo-expand-v2
date: 2026-04-24
analyst: branch-models-lead
verdict: REJECTED
confidence: medium
investment_grade: false
sector: GEO-EXPAND
---

[GEO-EXPAND] Supio GEO Expand v2 — REJECTED: 0/100 | EBITDA base=н/д | LTV/CAC=н/д | Ключевое преимущество: глобально понятный plaintiff legal workflow | Главный риск: в РФ нет подтверждённого category pull и standalone recurring economics.

# 06-verdict — Investment Verdict

## Итоговое решение
**REJECTED.**

Supio-подобный plaintiff-side legal AI не проходит для РФ как standalone GEO-EXPAND кейс. Боль вокруг претензий, страховых споров и медэкспертиз существует, но она упакована в услугу и low-ticket legal assistance, а не в отдельный software category с достаточным recurring economics.

## Почему кейс отклонён
1. **Demand остаётся LOW.** Все core и adjacent запросы через demand API дали LOW, даже когда я расширил проверку до автоюристов, Telegram и страховых споров.
2. **Нет локального category pull.** В РФ видны legal-help сервисы, но не видно устойчивого спроса на plaintiff workflow automation уровня Supio.
3. **Profit Gate FAIL.** Ни solo SaaS, ни team workflow, ни service-heavy hybrid не выводят компанию к EBITDA 500 тыс. ₽/мес при реалистичном buyer universe.
4. **Price compression слишком жёсткий.** Зарубежные аналоги продаются по $99-499/seat/month или usage-based, тогда как локальный рынок нормально платит 5-17 тыс. ₽ за юридический пакет, а не сотни тысяч рублей MRR за AI workflow.
5. **Buyer pool узкий.** Лучший локальный wedge это несколько legal factories и сервисов правовой поддержки, а не широкий класс plaintiff firms как в США.

## Что в кейсе сильное
- Глобально willingness to pay существует.
- Технологически use-case понятен: medical summary, demand package, chronology, intake-to-settlement workflow.
- В РФ есть adjacent legal demand и Telegram/legal-help инфраструктура.

## Почему этого всё равно недостаточно
Эти плюсы не складываются в fundable market. Локальный рынок не даёт ни достаточного количества покупателей, ни подходящего чека, ни короткого цикла продаж. В итоге даже хороший продукт остаётся слишком маленьким и services-like.

## Финальный статус для пайплайна
**Перевести кейс в `pipeline/rejected/`.**

## Основание решения
- `00-brief.md`
- `02-demand.md`
