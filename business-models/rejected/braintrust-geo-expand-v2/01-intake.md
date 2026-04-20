---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-braintrust-geo-expand.md
created: 2026-04-20T07:20:00+03:00
original_verdict: triage/triage-2026-04-19-braintrust-geo-expand.md
---

# Intake

## Статус
Принудительный rerun/resurrect. Кейс создан как отдельный `-v2` по standing orders и передаётся дальше в P3-demand-validation.

## Полный контекст из raw

# RESURRECT SIGNAL — braintrust-geo-expand

## Meta
- source: triage/triage-2026-04-19-braintrust-geo-expand.md
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
2026-04-19

## Входные данные
- `pipeline/raw/raw-2026-04-19-0127-msk-braintrust-geo-expand.md`

## Классификация
Новый сигнал, но новый кейс не открываем.

## Решение
Кейс не создан. Сигнал обработан без открытия нового кейса.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` не найдено: сигнал относится к AI observability / evals / tracing для production LLM и агентных систем, а существующие кейсы покрывают другие продуктовые и сервисные ниши.
- Сигнал сам по себе качественный: во входном файле зафиксированы сильные признаки рыночной валидации, включая Series B на 80 млн долларов при оценке 800 млн долларов в феврале 2026 года и публичные enterprise-референсы уровня Notion, Replit, Cloudflare, Ramp, Dropbox и Coursera.
- Однако экономика не проходит порог Program 1 для открытия нового кейса: указанный диапазон `900 000-4 800 000 ₽ в год` на одного клиента означает примерно `75 000-400 000 ₽ в месяц`, то есть ниже рабочего порога `> 500 000 ₽/мес.`.
- Во входном файле есть оговорка, что для банков, телекомов, интеграторов и внутренних AI-платформ LTV может быть выше за счёт on-prem/self-hosted и compliance-модулей, но на текущих данных этого недостаточно, чтобы уверенно открыть отдельный high-LTV кейс.

## Что сделано
- Новый кейс в `pipeline/cases/` не создавался.
- Создан triage-отчёт на русском языке.
- Исходный raw-файл обработан и перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал содержательный и подтверждает рост категории AI observability/evals, но на текущих данных не дотягивает до порога Program 1 по monthly potential, поэтому новый кейс не открываем.

```
