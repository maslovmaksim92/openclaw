---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-kintsugi-geo-expand.md
created: 2026-04-20T18:42:00+03:00
original_verdict: triage/triage-2026-04-19-kintsugi-geo-expand.md
---

# Intake

## Режим обработки
Принудительный полный пайплайн для файла с префиксом resurrect-. Кейс создан как новая версия независимо от прошлой классификации duplicate/supporting/new.

## Примечание
Создан принудительный rerun-case для повторного полного прохождения P3→P7. Историческое решение о неоткрытии кейса сохранено только как контекст для новой аналитики.

## Полный контекст из raw

# RESURRECT SIGNAL — kintsugi-geo-expand

## Meta
- source: triage/triage-2026-04-19-kintsugi-geo-expand.md
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
- `pipeline/raw/raw-2026-04-19-kintsugi-geo-expand.md`

## Классификация
Новый сигнал, но новый кейс не открываем.

## Решение
Кейс не создан. Сигнал отложен без открытия нового кейса.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` не найдено: сигнал относится к AI-native автоматизации косвенных налогов и filing для SMB e-commerce, SaaS и маркетплейс-продавцов, а не к уже открытым кейсам по GRC, enterprise compliance или transfer pricing.
- Сигнал качественный по спросу и подтверждён traction на западном рынке: в raw-файле указаны 2400 клиентов, выручка 3 млн долларов за 2024 год, цель превысить 10 млн долларов к концу 2025 года и churn 0,1%.
- Однако экономика не проходит порог Program 1 для открытия нового кейса: указанный диапазон `120 тыс. - 900 тыс. ₽ ARR` на клиента означает примерно `10 тыс. - 75 тыс. ₽ в месяц`, а даже для крупных платформ `1,5-4,0 млн ₽ в год` это около `125 тыс. - 333 тыс. ₽ в месяц`, то есть ниже рабочего порога `> 500 тыс. ₽/мес.`.
- Для локального рынка тема выглядит скорее как продуктовый SaaS или узкий taxtech-инструмент для SMB, чем как high-LTV операторская модель с достаточным monthly potential по standing orders Program 1.

## Что сделано
- Новый кейс в `pipeline/cases/` не создавался.
- Исходный raw-файл обработан и перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал не шум и не дубликат, но для Program 1 он слишком слаб по экономике: ниша выглядит интересной, однако текущий monthly potential не дотягивает до порога открытия нового кейса.

```
