# Verdict

Дата: 2026-05-12 23:20 MSK  
Стадия: Program 5 — Unit Economics  
Решение: **REJECTED**

## Причина решения

Кейс не проходит fund-level investment filter.

Ключевые причины:
1. **LTV/CAC = 2.31x**, что ниже минимального инвестиционного порога `3.0x`.
2. **Fully-loaded CAC = 388 608 ₽** на клиента для sales-assisted SMB service-модели.
3. При реалистичном fixed cost base и штатной команде **EBITDA 500k+/мес не достигается даже на 50 клиентах**.
4. Break-even наступает только около **97 клиентов**, а burn до этой точки слишком высок для данного типа бизнеса.

## Короткий вывод

Даже если спрос на managed websites существует и AI снижает себестоимость production, бизнес остаётся слишком людьмиёмким. Экономика ближе к агентству с AI-ускорением, чем к software-like recurring business.

## Формальный статус

- Program 5: **FAIL**
- Pipeline action: **move to `pipeline/rejected/`**

## Артефакты
- `04-economics.md`
- `06-verdict.md`
- `07-score-trajectory.md`
