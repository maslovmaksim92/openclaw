---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-raapid-medical-coding-geo-expand.md
created: 2026-04-21T13:33:00+03:00
---

# 01-intake

## Кейс
raapid-medical-coding-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-14-raapid-medical-coding-geo-expand.md

## Краткий контекст
Standalone GEO-EXPAND кейс по autonomous medical coding, audit readiness и revenue cycle automation. Исходный triage считал сигнал supporting для существующего кейса, но resurrect требует новой полной оценки.

## Следующий шаг
Передать кейс в P3-demand-validation для полной переоценки по обновлённой системе анализа.

## Полный контекст из raw

# RESURRECT SIGNAL — raapid-medical-coding-geo-expand

## Meta
- source: triage/triage-2026-04-14-raapid-medical-coding-geo-expand.md
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
- pipeline/raw/raw-2026-04-14-raapid-medical-coding-geo-expand.md

## Классификация
поддерживающий сигнал для существующего кейса

## Решение
Обогатить существующий кейс: `autonomous-medical-coding-operator`.

## Почему
- В `pipeline/cases/` уже есть открытый кейс по автономному медицинскому кодированию, quality assurance и revenue cycle automation в медицинских организациях.
- Сигнал по RAAPID совпадает по нише, buyer profile и типу workflow: medical coding, risk adjustment, audit readiness и автоматизация высокостоимостных медицинских back-office процессов.
- Это не новый кейс, а сильный supporting signal: он даёт второе независимое подтверждение категории после CodaMetrix и усиливает гипотезу, что вокруг AI-медкодинга существует enterprise-ready и high-LTV сервисный слой.

## Что добавлено в кейс
В `pipeline/cases/autonomous-medical-coding-operator/01-evidence.md` добавлен supporting signal по RAAPID:
- дата и ссылка на источник VentureBeat;
- подтверждение, что категория поддерживается не одним игроком, а несколькими сильными компаниями;
- факты про Series A extension, стратегических инвесторов M12 и UPMC, Microsoft Healthcare AI certification и кейс Fortune 500 health system с потенциальным эффектом 5-15 млн долларов в год у клиента;
- уточнение, что локальный LTV-сигнал 3-12 млн руб. в год на клиента поддерживает high-LTV гипотезу кейса.

## Итог
Кейс обогащён: добавлено новое доказательство коммерческой зрелости и enterprise-ценности категории autonomous medical coding. Исходный raw-файл нужно перенести в `pipeline/raw/processed/`.

```

