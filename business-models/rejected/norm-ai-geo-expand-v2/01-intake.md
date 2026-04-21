---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-norm-ai-geo-expand.md
created: 2026-04-21T03:36:00+03:00
---

# 01-intake

## Кейс
norm-ai-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл с префиксом `resurrect-` по standing orders обязан пройти заново как самостоятельный кейс, даже если раньше был supporting signal, duplicate или candidate под другим кейсом.

## Ссылка на исходный verdict
triage/triage-2026-04-17-norm-ai-geo-expand.md

## Краткий контекст
Norm Ai как кандидат на enterprise compliance operations, policy execution и regulatory workflow automation в логике geo-expand.

## Следующий шаг
Кейс создан в intake и должен быть передан дальше в P3-demand-validation без повторной duplicate-классификации.

## Полный контекст из raw

# RESURRECT SIGNAL — norm-ai-geo-expand

## Meta
- source: triage/triage-2026-04-17-norm-ai-geo-expand.md
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
2026-04-17

## Входные данные
- `pipeline/raw/raw-2026-04-17-norm-ai-geo-expand.md`

## Классификация
Новый high-LTV кейс.

## Решение
Создан кейс `enterprise-compliance-operations-agents` в `pipeline/cases/`.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` по enterprise compliance-операциям и AI-агентам для policy-driven workflow не найдено.
- Сигнал не является шумом: во входном файле зафиксированы сильные признаки рыночной валидации, включая раунд 48 млн долларов, партнёрства с Microsoft и Prudential Financial, а также фокус на Fortune 100 и институтах с активами более 30 трлн долларов.
- Это отдельный enterprise-класс, а не просто точечный legaltech: продукт переводит нормативные требования и внутренние policy в исполняемый слой compliance-операций внутри рабочих процессов.
- По экономике сигнал проходит порог Program 1: ориентир 3,0-15,0 млн рублей в год на клиента соответствует примерно 250 000-1 250 000 рублей в месяц, а верхняя часть диапазона превышает порог 500 000 рублей в месяц.
- Локализация выглядит тяжёлой и сервисно-ёмкой, что поддерживает гипотезу о дорогих внедрениях и длительном recurring-сопровождении.

## Что сделано
- Создан `pipeline/cases/enterprise-compliance-operations-agents/00-brief.md` на русском языке.
- Создан `pipeline/cases/enterprise-compliance-operations-agents/01-evidence.md` с первичным сигналом на русском языке.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал по Norm Ai признан новым high-LTV кейсом. Кейс `enterprise-compliance-operations-agents` открыт для дальнейшей проработки.

```

