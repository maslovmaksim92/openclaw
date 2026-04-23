# 06-verdict

[GEO-EXPAND] SuperDial GEO Expand v2 — REJECTED: 34/100 | Спрос в РФ по payer-facing healthcare voice automation остаётся LOW, а Profit Gate не проходит ни в одном реалистичном сценарии.

## Вердикт
**REJECTED**

## Почему
- Обязательный demand endpoint по релевантным русскоязычным запросам вернул LOW. [T2]
- В РФ покупают более простой слой: запись, напоминания, Telegram-боты, AI-администратор, но не выраженный US-style insurance billing call workflow. [T2]
- Публичные цены аналогов и локальных substitute-решений показывают слишком низкий price ceiling для прохода EBITDA >= 500 тыс. ₽/мес. [T1][T2]
- Profit Gate fail во всех рассмотренных сценариях: low-ticket SaaS, mid-market automation, enterprise managed rollout. [T2]

## Решение
Остановить кейс на этапе P4 Demand Validation, зафиксировать reject и переместить папку в `pipeline/rejected/superdial-geo-expand-v2/`.

## Что могло бы изменить решение
- Публичные подтверждения крупных контрактов в РФ именно на healthcare payer/provider phone workflow, а не только на запись пациентов. [T2]
- Несколько локальных кейсов с ACV не ниже 1.5–3.0 млн ₽ в год на клиента и повторяемым sales motion. [T2]
- Доказательство, что продукт продаётся как broader revenue-ops / contact-center platform с интеграциями и service layer, а не как дешёвый receptionist bot. [T2]
