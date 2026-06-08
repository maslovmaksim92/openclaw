---
stage: verdict
case: podari-track-quick-ai-v2
date: 2026-06-08
analyst: branch-models-lead
verdict: REJECTED
confidence: medium
---

[QUICK-AI] Podari Track — REJECTED: 44/100 | спрос на персональные AI-песни в РФ подтверждён, но низкий чек, LTV/CAC 1,22x и отрицательный first-order contribution не дают investment-grade economics.

# 06-verdict — Final Verdict

## Вердикт
**REJECTED**

## Почему
Podari Track подтверждает, что в РФ есть реальный спрос на персональные AI-песни как consumer gifting продукт. Но фондовый порог этот кейс не проходит.

### Ключевые причины reject
1. **Profit Gate FAIL:** при 50 платящих клиентах/мес продукт не может приблизиться к EBITDA 500k+/мес.
2. **LTV/CAC = 1,22x**, что сильно ниже инвестиционного порога **3:1**.
3. **First-order contribution after CAC отрицательный**: новый клиент в base-case убыточен на первом заказе.
4. Экономика держится на repeat/referral и сезонных поводах, а не на устойчивом recurring revenue.
5. Открытые финансовые данные по юрлицу показывают, что даже при значимом масштабе прибыльность остаётся тонкой. [T1]

## Что в кейсе хорошего
- Спрос и willingness-to-pay есть.
- Telegram-first дистрибуция рабочая.
- Продукт понятный и быстрый.
- Категория коммерчески валидирована локально.

## Почему этого недостаточно для фонда
Для фонда нужен актив, который выдерживает покупной рост и даёт запас по unit economics. Здесь:
- чек слишком низкий,
- acquisition pressure слишком высокий,
- moat слабый,
- retention/повторные покупки слишком ненадёжны.

## Финальное решение по pipeline
- Создать `04-economics.md`: выполнено.
- Зафиксировать `REJECTED`: выполнено.
- Переместить кейс в `pipeline/rejected/`: требуется и выполняется в этом cycle.

## Источники
- [T1] https://www.tbank.ru/business/contractor/legal/1197746132902/
- [T2] https://podari-track.ru/
- [T3] `04-economics.md`
