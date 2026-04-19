# Verdict — Voice Accent Translation Contact Center Operator

## Решение
**❌ REJECTED**

## Основание
Кейс попадает под правило раннего отклонения: **DEMAND = LOW** по `multi-demand`, а **Profit Gate FAIL** во всех проверенных сценариях монетизации, то есть достижимый **EBITDA >= 500 тыс. ₽/мес** не просматривается на реалистичном горизонте для РФ.

## Ключевые причины
1. Категория почти не видна в RU demand signals.
2. Есть подтвержденный бюджет на contact-center стек, но не на отдельный accent-translation line item.
3. Рынок узкий, enterprise-heavy и дорогой в продаже.
4. Unit economics не проходят порог даже при оптимистичном pricing.

## Сравнение с прошлым rerun
- previous_status: ❌ REJECTED
- previous_score: n/a
- new_status: ❌ REJECTED
- delta_vs_previous: статус не улучшился; rerun с более строгим Source Tiering и TAM/SAM/SOM подтверждает исходное отклонение.

## Следующее действие
Перенести кейс в `pipeline/rejected/`.
