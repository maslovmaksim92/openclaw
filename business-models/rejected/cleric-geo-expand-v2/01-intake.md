---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-cleric-geo-expand.md
created: 2026-04-20T08:44:00+03:00
---

# 01-intake

## Кейс
cleric-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-18-cleric-geo-expand-duplicate.md

## Краткий контекст
Standalone GEO-EXPAND кейс по autonomous SRE, root cause analysis и self-learning operational memory. Исходный triage считал сигнал supporting/duplicate и ниже порога Program 1, но rerun требует новой полной оценки.

## Следующий шаг
Передать кейс в P3-demand-validation: проверить enterprise budget, частоту боли, on-prem требования, managed service слой и реалистичность high-LTV модели на рынке РФ.

## Полный контекст из raw

# RESURRECT SIGNAL — cleric-geo-expand

## Meta
- source: triage/triage-2026-04-18-cleric-geo-expand-duplicate.md
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
2026-04-18

## Входные данные
- `pipeline/raw/raw-2026-04-18-0127-msk-cleric-geo-expand.md`

## Классификация
дубликат / supporting signal по уже известной категории autonomous SRE

## Решение
Новый кейс не открывать и существующие открытые кейсы не обогащать.

## Почему
- Сигнал повторно подтверждает ту же модель: AI-native SRE-платформа для автономного расследования production-инцидентов, root cause analysis и накопления operational memory.
- В `pipeline/cases/` по-прежнему нет подходящего открытого кейса для обогащения через `01-evidence.md`.
- Ближайшее содержательное совпадение остаётся в уже утверждённой категории `pipeline/approved/autonomous-sre-incident-response-operator`, поэтому отдельный новый case не нужен.
- По входному файлу `ltv_signal` указан как `1200000-6000000 ₽ в год с одного enterprise-клиента`, то есть примерно `100000-500000 ₽ в месяц`. Это не превышает порог `> 500000 ₽ в месяц`, требуемый для открытия нового кейса в Program 1.

## Что сделано
- Новый кейс не создавался.
- `01-evidence.md` не обновлялся, потому что совпадающего открытого кейса в `pipeline/cases/` нет.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал полезный как дополнительное подтверждение интереса к категории self-learning AI SRE, но для Program 1 он остаётся дубликатом без основания для открытия нового кейса. Имеет смысл вернуться к теме, если появятся данные о чеке выше `500000 ₽ в месяц`, локальном спросе со стороны крупных российских инфраструктурных команд или более широком services/on-prem слое, который поднимет LTV выше порога.
```
