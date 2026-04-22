---
sector: AI-SERVICES
rerun: true
source_raw: 2026-04-19-resurrect-resolve-ai-sre.md
created: 2026-04-21T13:33:00+03:00
---

# 01-intake

## Кейс
resolve-ai-sre-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-14-resolve-ai-sre.md

## Краткий контекст
Standalone AI-SERVICES кейс по AI SRE, production incident investigation и ускорению MTTR. Исходный triage отклонил сигнал из-за пограничного LTV, но resurrect требует новой полной оценки.

## Следующий шаг
Передать кейс в P3-demand-validation для полной переоценки по обновлённой системе анализа.

## Полный контекст из raw

# RESURRECT SIGNAL — resolve-ai-sre

## Meta
- source: triage/triage-2026-04-14-resolve-ai-sre.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Триаж

## Дата
2026-04-14

## Входные данные
- pipeline/raw/raw-2026-04-14-resolve-ai-sre.md

## Классификация
новый сигнал, отклонён на этапе triage

## Решение
Не создавать новый кейс.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` не найдено: сигнал относится к категории AI SRE / production engineering / incident response, а текущие активные кейсы покрывают другие функции и вертикали.
- По самому raw-файлу подтверждённый чек ниже обязательного порога для запуска нового кейса: указан `ltv_signal: 1800000-6000000 RUB в год с клиента`, то есть примерно 150 000-500 000 руб/мес. Это не подтверждает LTV Gate `> 500 000 руб/мес`.
- Сигнал качественный и выглядит как реальная GEO-EXPAND возможность для enterprise DevOps/SRE рынка, но на текущих данных он остаётся пограничным по экономике, а не заведомо проходным.
- Для создания кейса не хватает более сильного подтверждения, что в РФ можно системно продавать контур за пределами 500 000 руб/мес, например через multi-team rollout, on-prem deployment или дорогой managed service поверх observability stack.

## Итог
Сигнал обработан и отклонён на этапе triage по причине недостаточно подтверждённого LTV для нового кейса. Raw-файл перемещён в `pipeline/raw/processed/`, новый кейс не создан.

```

