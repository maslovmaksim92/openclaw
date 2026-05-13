---
sector: QUICK-AI
rerun: true
source_raw: 2026-04-19-resurrect-ivoxstudio-quick-ai.md
created: 2026-04-20T18:42:00+03:00
original_verdict: triage/triage-2026-04-19-ivoxstudio-quick-ai.md
---

# Intake

## Режим обработки
Принудительный полный пайплайн для файла с префиксом resurrect-. Кейс создан как новая версия независимо от прошлой классификации duplicate/supporting/new.

## Примечание
Создан принудительный rerun-case для повторного полного прохождения P3→P7. Исходный verdict о supporting signal сохранён как исторический контекст, но не используется как итоговое решение.

## Полный контекст из raw

# RESURRECT SIGNAL — ivoxstudio-quick-ai

## Meta
- source: triage/triage-2026-04-19-ivoxstudio-quick-ai.md
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
- pipeline/raw/raw-2026-04-19-0933-msk-ivoxstudio-quick-ai.md

## Классификация
дубликат / supporting signal для существующего кейса

## Решение
Обогатить существующий кейс: `self-serve-ai-voiceover-service`.

## Почему
- Тематика полностью совпадает с уже открытым кейсом self-serve AI-озвучки: генерация озвучки из текста через Telegram, веб и API.
- Сигнал не открывает новую отдельную категорию, а усиливает уже существующую гипотезу дополнительным локальным игроком с рабочей монетизацией.
- Комбинация B2C-подписок и B2B/API-слоя дополнительно подтверждает, что у кейса есть путь к EBITDA выше 500 000 ₽ в месяц.

## Что добавлено в кейс
- Создан и заполнен файл `pipeline/cases/self-serve-ai-voiceover-service/01-evidence.md`.
- Добавлен supporting signal по iVox Studio / iVoxOfficialBot.
- Зафиксированы ключевые факты: 10 645 monthly users в Telegram, тарифы 390 ₽, 2 990 ₽ и 11 990 ₽ в месяц, а также наличие API / интеграционного слоя.

## Что сделано
- Кейс `self-serve-ai-voiceover-service` обогащён.
- Raw-файл обработан и должен быть перемещён в `pipeline/raw/processed/`.

## Вердикт
Сигнал засчитан как supporting signal для существующего кейса AI-озвучки. Он усиливает уверенность в локальном спросе, жизнеспособной монетизации и наличии более высокого LTV за счёт API и white-label сценариев.

```
