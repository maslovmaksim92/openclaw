# 06-verdict

[GEO-EXPAND] 0527 MSK Sanas GEO Expand v2 — REJECTED: 0/100 | standalone demand в РФ не подтверждён, Profit Gate FAIL, отдельный fund-grade wedge не доказан.

## Кейс
0527-msk-sanas-geo-expand-v2

## Вердикт
**REJECTED на Program 4 (Demand Validation).**

## Почему
1. Mandatory demand API по четырём релевантным keyword-проверкам дал **LOW / score=0**.
2. В РФ не найден сформированный B2B budget line именно под accent translation для contact center.
3. Конкуренты с ценами существуют, но это в основном global adjacent tooling, а не локально доказанный enterprise wedge.
4. Profit Gate не проходит ни в self-serve, ни в mid-market managed, ни в enterprise high-touch сценарии.
5. Следовательно, правило early reject выполнено полностью: **DEMAND=LOW + Profit Gate FAIL**.

## Инвестиционный вывод
Глобально тема real-time accent conversion выглядит технологически интересной, но для локального standalone entry в РФ/СНГ кейс слишком узкий и слишком зависимый от импортированного спроса. Для фонда это не проходит как самостоятельный demand-led wedge.

## Сравнение с прежним routing-решением
Предыдущее решение routing в общий кейс `voice-accent-translation-contact-center-operator` было оправданным: как supporting signal Sanas усиливает глобальную категорию, но как отдельный локальный pipeline-case сейчас не выдерживает demand-gate.

## Статус
Перенести в `pipeline/rejected/`.
