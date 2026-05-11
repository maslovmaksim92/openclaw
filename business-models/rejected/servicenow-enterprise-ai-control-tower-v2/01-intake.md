---
sector: B2B-OPS
rerun: true
source_raw: 2026-04-19-resurrect-servicenow-enterprise-ai-control-tower.md
created: 2026-04-21T20:36:00+03:00
original_verdict_source: triage/triage-2026-04-14-servicenow-enterprise-ai-control-tower.md
---

# Intake

## Статус
Принудительный полный пайплайн по правилу resurrection. Кейс создан как новый standalone candidate, без классификации как duplicate на этапе intake.

## Исходный raw-файл

# RESURRECT SIGNAL — servicenow-enterprise-ai-control-tower

## Meta
- source: triage/triage-2026-04-14-servicenow-enterprise-ai-control-tower.md
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
- pipeline/raw/raw-2026-04-14-servicenow-enterprise-ai-control-tower.md

## Классификация
поддерживающий сигнал для существующего кейса

## Решение
Обогатить существующий кейс: `enterprise-agent-control-plane-implementation-operator`.

## Почему
- Сигнал относится не к узкому workflow, а к широкому enterprise AI platform слою, где ценность формируется вокруг governance, масштабирования, интеграции и эксплуатации AI-продуктов в большом аккаунте.
- ServiceNow даёт финансовое подтверждение платёжеспособного спроса: сотни крупных ACV-сделок и отдельное указание, что крупнейшие сделки уже включают несколько AI-продуктов.
- Это усиливает именно кейс про enterprise agent control plane / AI platform implementation, потому что показывает готовность крупных клиентов платить не только за эксперимент, но и за промышленный AI stack с длинным циклом сопровождения.
- Для service business это важный сигнал в пользу крупных внедренческих и managed service контрактов поверх enterprise AI platform, а не просто разовых пилотов.

## Что добавлено в кейс
В `pipeline/cases/enterprise-agent-control-plane-implementation-operator/01-evidence.md` добавлен supporting signal от ServiceNow с датой, ссылкой на источник и ключевыми фактами:
- 244 сделки с net new ACV свыше 1 млн долларов за квартал, +38% год к году;
- 603 клиента с ACV свыше 5 млн долларов, +20% год к году;
- крупнейшие сделки включали минимум пять AI-продуктов;
- net new ACV у Now Assist более чем удвоился год к году;
- cRPO вырос на 25% до 12,85 млрд долларов.

## Итог
Кейс обогащён: добавлено финансовое подтверждение крупного enterprise-спроса и сервисной ёмкости вокруг AI platform / control plane слоя.
```

