---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-linq-geo-expand.md
created: 2026-04-20T22:33:00+03:00
---

# 01-intake

## Кейс
linq-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-18-linq-geo-expand.md

## Краткий контекст
Standalone кейс по AI-native messaging infrastructure для agentic customer communication и enterprise support funnels. Требуется новая аналитика P3→P7, даже если исторически сигнал считался дубликатом или недостаточным по LTV.

## Следующий шаг
Передать кейс в P3-demand-validation: подтвердить high-LTV сценарии, сложность локализации, доступность buyer'ов и наличие устойчивого GEO-EXPAND окна.

## Полный контекст из raw

# RESURRECT SIGNAL — linq-geo-expand

## Meta
- source: triage/triage-2026-04-18-linq-geo-expand.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Триаж: Linq, GEO-EXPAND

## Статус
Новый сигнал, кейс не создан.

## Решение
Отклонено на этапе Intake and Triage.

## Причина
Сигнал сам по себе качественный: у Linq есть сильная внешняя валидация, заметный рост, крупный раунд и понятный продуктовый тезис вокруг AI-native messaging infrastructure. Но по входной оценке коммерческий потенциал для локального кейса в РФ составляет 900 тыс. - 3,6 млн ₽ в год с одного среднего или крупного клиента, то есть примерно 75 тыс. - 300 тыс. ₽ в месяц. Это ниже порога Program 1, который требует потенциал LTV свыше 500 тыс. ₽ в месяц.

## Что зафиксировано
- Категория: инфраструктура для AI-ассистентов и агентских сценариев внутри мессенджеров и других нативных каналов общения.
- Сильные факты из сигнала: 30+ млн сообщений в месяц, 134 000 MAU, 295% net revenue retention, zero churn, Series A на $20 млн.
- Локализация для РФ выглядит реалистичной через Telegram, WhatsApp Business, web-chat, voice и SMS, но unit economics по входному сигналу пока недостаточны для прохождения фильтра Program 1.

## Итог
Raw-файл обработан и перемещён в pipeline/raw/processed/. Новый кейс в pipeline/cases/ не создавался.

```

