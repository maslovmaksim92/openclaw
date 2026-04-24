---
sector: FINTECH
rerun: true
source_raw: 2026-04-19-resurrect-corgi-startup-insurance-geo-expand.md
created: 2026-04-20T11:18:00+03:00
---

# 01-intake

## Кейс
corgi-startup-insurance-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-14-corgi-startup-insurance-geo-expand.md

## Краткий контекст
Standalone insurtech-кейс по AI-native underwriting и обслуживанию страховых программ для стартапов и технологических компаний. Требуется новая аналитика P3→P7, даже если раньше сигнал считался слабым по unit economics.

## Следующий шаг
Передать кейс в P3-demand-validation: подтвердить high-LTV сценарии, сложность локализации, доступность buyer'ов и наличие устойчивого GEO-EXPAND окна.

## Полный контекст из raw

# RESURRECT SIGNAL — corgi-startup-insurance-geo-expand

## Meta
- source: triage/triage-2026-04-14-corgi-startup-insurance-geo-expand.md
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
- pipeline/raw/raw-2026-04-14-corgi-startup-insurance-geo-expand.md

## Классификация
низкий LTV для Program 1, кейс не открываем

## Решение
Не открывать новый кейс и не обогащать существующие кейсы.

## Почему
- Сигнал описывает AI-native страховщика для стартапов и технологических компаний, но в raw-файле указана экономика `120000-600000 RUB в год на одного клиента`, то есть примерно 10 000-50 000 руб. в месяц на типичный SMB/startup аккаунт.
- Даже верхняя часть базового диапазона значительно ниже порога Program 1 `> 500 000 руб./мес.` на клиента.
- Потенциал upsell для быстрорастущих tech-компаний в raw-файле упомянут качественно, но не подтверждён числами, достаточными для открытия high-LTV кейса.
- Подходящего открытого кейса в `pipeline/cases/` по AI-страхованию стартапов / digital underwriting для tech-risk сейчас нет, поэтому обогащать существующий кейс нечем.
- Локализация остаётся тяжёлой из-за регуляторики, лицензирования и зависимости от партнёрств со страховщиками, что дополнительно ухудшает профиль запуска при текущем LTV.

## Что сделано
- Новый кейс не создан.
- Существующие кейсы не обновлялись.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал стратегически интересный как GEO-EXPAND идея для insurtech, но для Program 1 он слишком слабый по unit economics: при текущем подтверждённом LTV открывать кейс рано.
```

