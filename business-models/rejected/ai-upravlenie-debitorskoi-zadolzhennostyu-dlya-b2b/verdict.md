---
stage: verdict
updated: 2026-04-24T21:47:00+03:00
verdict: REJECTED
---

[FINTECH] AI-управление дебиторской задолженностью для B2B — REJECTED: 58/100 | demand подтверждён, но при ARPU 65 тыс. ₽/мес модель требует слишком тяжёлой команды и не проходит Profit Gate.


# 06-verdict

## Решение
**REJECTED**

## Почему
Кейс проходит demand-stage, но не проходит investment-grade economics:

1. **Profit Gate FAIL.** При реалистичном mid-market B2B сценарии и чеке 65 тыс. ₽/мес модель требует около **104 клиентов до break-even**. При **50 клиентах EBITDA остается около -2,47 млн ₽/мес**, то есть порог **>500 тыс. ₽/мес EBITDA** недостижим.
2. **Слишком тяжелая команда для данного ARPU.** Безопасный fintech-like продукт поверх 1С, ЭДО и банковских данных требует CTO, backend, DevOps, implementation, sales и customer success. Такой cost base не окупается на раннем масштабе.
3. **CAC недооценивался на intake.** Fully-loaded CAC по blended модели получается **~323 917 ₽**, что существенно выше ballpark из intake.
4. **Продукт выглядит ближе к productized service, чем к чистому software-layer.** Демо, интеграции, security review, настройка workflow и ручные исключения делают motion дорогим и медленным.

## Что должно измениться для revisit
- Поднять ARPU минимум к **120–150 тыс. ₽/мес** за счет более крупного сегмента или transaction-based pricing.
- Сильно упростить onboarding и интеграции, чтобы снизить implementation load.
- Перейти в партнерский channel-first motion через 1С-интеграторов и финансовый аутсорсинг с более дешевым CAC.
- Доказать, что продукт может обслуживать клиента с COGS < 12 тыс. ₽/мес и без heavy-touch CSM.

## Финальный статус
**Отклонить и перенести в `pipeline/rejected/`.**