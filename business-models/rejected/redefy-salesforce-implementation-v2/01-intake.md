---
sector: B2B-OPS
rerun: true
source_raw: 2026-04-19-resurrect-redefy-salesforce-implementation.md
created: 2026-04-21T15:12:11+03:00
---

# 01-intake

## Кейс
redefy-salesforce-implementation-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом , поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-10-redefy-salesforce-implementation.md

## Краткий контекст
Standalone кейс по AI-native implementation operator вокруг Salesforce Agentforce и Industry Cloud: ускоренное внедрение агентного стека поверх большой enterprise-платформы с интеграциями и аналитическим слоем.

## Следующий шаг
Передать кейс в P3-demand-validation: проверить глубину бюджета в экосистеме Salesforce, воспроизводимость внедренческой модели и реалистичность высокого LTV через implementation плюс managed services.

## Полный контекст из raw

# RESURRECT SIGNAL — redefy-salesforce-implementation

## Meta
- source: triage/triage-2026-04-10-redefy-salesforce-implementation.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Triage

## Date
2026-04-10

## Inputs
- pipeline/raw/processed/radar-2026-04-10-2210-msk.md

## Classification
signal, new case candidate

## Decision
Создать новый case: `pipeline/cases/ai-native-salesforce-implementation-operator/`.

## Why
Сигнал описывает не просто общий enterprise AI adoption, а более конкретную сервисно-операторскую модель: AI-native фирма, которая ускоряет внедрение Salesforce Agentforce и Industry Cloud с помощью собственного agentic implementation engine и аналитиков.

Это отличается от уже открытых кейсов по двум причинам:
- фокус не SMB generalist, а enterprise Salesforce ecosystem с существующим бюджетом и сложной интеграцией;
- value proposition не только консалтинг, а ускоренное и более стандартизируемое внедрение agent stack поверх крупной установленной платформы.

## Triage note
Пока это early evidence по модели AI-native implementation operator вокруг большого software base. Дальше нужно проверить, это единичный services-branding signal или начало воспроизводимого рынка/категории.
```
