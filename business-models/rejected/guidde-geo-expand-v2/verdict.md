---
stage: verdict
updated: 2026-04-22T23:45:13+03:00
verdict: REJECTED
case: guidde-geo-expand-v2
sector: GEO-EXPAND
---

# 06-verdict

[GEO-EXPAND] Guidde GEO Expand v2 — REJECTED: 58/100 | LTV/CAC выглядит хорошо, но при 50 клиентах кейс не даёт требуемый EBITDA > 500 тыс. ₽/мес и остаётся слишком чувствительным к execution risk.

## Итог
- **Вердикт: REJECTED**
- **Причина**: кейс не проходит обязательный **Profit Gate** на уровне фонда.

## Почему reject
1. **LTV/CAC** у модели хороший, **9,1x**, то есть проблема не в качестве одного клиента.
2. Но при fully-loaded fixed-cost базе и реалистичном найме компания выходит только примерно в ноль на **50 клиентах**.
3. По standing order кейс должен показывать **EBITDA не ниже +500 тыс. ₽/мес уже на 50 клиентах**, иначе это reject.
4. Следовательно, модель слишком чувствительна к execution risk: нужен либо более высокий ARPA, либо более дешёвый GTM, либо существенно более лёгкая команда.

## Что именно сломало экономику
- высокая fixed-cost база из product + GTM команды;
- недостаточный запас прочности между contribution profit и постоянными расходами;
- отсутствие PLG/viral distribution, из-за чего acquisition остаётся дорогим и service-led.

## Что могло бы перевести кейс в pass
- ARPA ближе к **200k+ ₽/мес**;
- dominantly partner-led CAC вместо outbound-heavy motion;
- более узкий продуктовый scope и меньшая команда до достижения 20-25 клиентов.

## Связанный артефакт
- `pipeline/cases/guidde-geo-expand-v2/04-economics.md`
