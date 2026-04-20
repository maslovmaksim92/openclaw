---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-aaru-geo-expand.md
created: 2026-04-20T04:42:12+03:00
---

# 01-intake

## Кейс
aaru-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-17-aaru-geo-expand.md

## Краткий контекст
Standalone GEO-EXPAND кейс по synthetic customer research и synthetic populations для enterprise research и marketing insights. Нужно проверить спрос, интеграционную сложность и реалистичность high-LTV локализации на рынке РФ.

## Следующий шаг
Передать кейс в P3-demand-validation: проверить buyer, бюджет, частоту использования, интеграции в research/insights workflow и фактическое окно GEO-EXPAND для РФ.

## Полный контекст из raw

# RESURRECT SIGNAL — aaru-geo-expand

## Meta
- source: triage/triage-2026-04-17-aaru-geo-expand.md
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
- `pipeline/raw/raw-2026-04-17-0127-msk-aaru-geo-expand.md`

## Классификация
Новый кейс.

## Решение
Создан новый кейс `synthetic-customer-research-agentic-prediction` в `pipeline/cases/`.

## Почему это не дубль
В `pipeline/cases/` не найден открытый кейс с фокусом именно на synthetic customer research, synthetic populations и agentic prediction для enterprise research и marketing insights. Существующий кейс про warehouse-native AI decisioning для маркетинга решает другую задачу: активацию данных и orchestration поверх DWH, а не моделирование синтетических аудиторий и замену части исследовательского контура.

## Почему кейс проходит фильтр
- Во входном материале зафиксирован сильный коммерческий сигнал: Series A при headline-оценке 1 млрд долларов в декабре 2025 года.
- Подтверждено стратегическое партнёрство с Accenture, что усиливает enterprise go-to-market сигнал.
- Указаны клиенты и пилоты уровня EY, McDonald’s, Bayer, Boston Beer, A24 и Coca-Cola, что снижает риск того, что это нишевая игрушка без платёжеспособного спроса.
- Во входном материале указан локальный LTV 2,4-12,0 млн ₽ в год на клиента, то есть верхняя часть диапазона превышает порог 500 000 ₽ в месяц.
- Для РФ не найден прямой зрелый аналог с таким же позиционированием, что оставляет окно для service-led локализации.

## Что создано
- `pipeline/cases/synthetic-customer-research-agentic-prediction/00-brief.md`

## Статус raw-файла
Файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Создан новый кейс по synthetic customer research и agentic prediction для enterprise-сегмента с потенциально высоким чеком на российском рынке.

```

