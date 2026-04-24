---
stage: verdict
case: superdial-insurer-calls-geo-expand-v2
date: 2026-04-24
analyst: branch-models-lead
verdict: REJECTED
confidence: medium
investment_grade: false
sector: HEALTHCARE
---

[HEALTHCARE] SuperDial insurer calls GEO Expand v2 — REJECTED: 0/100 | EBITDA base=н/д | LTV/CAC=н/д | Ключевое преимущество: реальный adjacent рынок ДМС и clinic ops | Главный риск: standalone payer-call automation не подтверждает локальный спрос и economics.

# 06-verdict — Investment Verdict

## Итоговое решение
**REJECTED.**

SuperDial-подобный insurer-call automation кейс не проходит demand-stage для РФ. Проблема не в отсутствии любого healthcare spend, а в том, что локальный рынок monetizes ДМС, запись и patient communication, но не показывает достаточного спроса на standalone payer-call / denial-management / prior-authorization automation.

## Почему кейс отклонён
1. **Exact-demand низкий.** Обязательный multi-demand по ключам insurer-call workflow в РФ дал LOW; MEDIUM есть только по широкому adjacent keyword `дмс клиника`.
2. **WTP доказан только для смежных clinic ops, а не для точного продукта.** Публичные конкуренты дают price anchor в низком диапазоне и показывают commoditization voice layer.
3. **Profit Gate не проходит.** Self-serve и mid-market сценарии не дают надёжного пути к EBITDA ≥ 500 тыс. ₽/мес, а enterprise сценарий требует product pivot и не подтверждён локальным спросом.
4. **Рынок ДМС большой, но addressable software wedge маленький.** Нельзя путать 191,3 млрд ₽ премий с investable размером категории insurer-call automation.

## Что в кейсе всё же настоящее
- ДМС и координация со страховщиками в РФ существуют как рабочий операционный контур.
- У клиник и страховщиков действительно есть ручные процессы, звонки и статусы.
- Telegram и voice automation уже monetized в смежных clinic ops задачах.

## Ключевой инвестиционный вывод
Как standalone GEO-EXPAND в РФ этот кейс слишком узкий и плохо локализуемый. Если и строить бизнес, то уже не как SuperDial-as-is, а как более широкий DMS workflow / clinic operations platform. Это другой кейс и другой продуктовый тезис.

## Финальный статус для пайплайна
**Остановить кейс на этапе P4 Demand Validation, записать reject и переместить папку в `pipeline/rejected/superdial-insurer-calls-geo-expand-v2/`.**

## One-liner для инвесткомитета
**SuperDial в РФ упирается в слабый локальный спрос на payer-call automation: adjacent рынок ДМС есть, но standalone economics и category pull для продукта не подтверждены.**

## Основание решения
- `00-brief.md`
- `02-demand.md`
