---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-guidde-geo-expand.md
created: 2026-04-20T16:33:33+03:00
original_verdict: triage/triage-2026-04-19-guidde-geo-expand.md
---

# 01-intake

## Кейс
guidde-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-19-guidde-geo-expand.md

## Краткий контекст
Сигнал `guidde-geo-expand` переоткрыт как standalone candidate для нового полного прохода P3→P7 с обновлённой системой аналитики.

## Следующий шаг
Кейс создан в intake и должен быть передан дальше в P3-demand-validation без повторной duplicate-классификации.

## Полный контекст из raw

# RESURRECT SIGNAL — guidde-geo-expand

## Meta
- source: triage/triage-2026-04-19-guidde-geo-expand.md
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
- `pipeline/raw/raw-2026-04-19-0903-msk-guidde-geo-expand.md`

## Классификация
Поддерживающий сигнал для существующего открытого кейса.

## Решение
Сигнал добавлен в кейс `enterprise-ai-video-production-operator`.

## Что именно добавлено
- Создан и заполнен файл `pipeline/cases/enterprise-ai-video-production-operator/01-evidence.md`.
- Добавлен supporting signal по Guidde с датой, источниками, объяснением, почему сигнал усиливает кейс, и ключевыми фактами.
- Зафиксировано, что категория AI-видео для бизнеса включает не только marketing/video generation сценарии, но и repeatable enterprise workflow для onboarding, software adoption, customer support и обучения.

## Почему это усиливает кейс
Guidde показывает, что enterprise AI video category опирается не только на креативный продакшн, но и на операционные видеоформаты с регулярным спросом внутри компаний. Это расширяет адресуемый рынок кейса и снижает риск, что модель ограничится только дорогими маркетинговыми или студийными use case.

## Статус raw-файла
Файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Кейс обогащён: добавлен подтверждающий GEO-EXPAND сигнал по Guidde для `enterprise-ai-video-production-operator`.

```
