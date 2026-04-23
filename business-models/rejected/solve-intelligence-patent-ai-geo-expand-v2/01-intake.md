---
sector: LEGAL
rerun: true
source_raw: 2026-04-19-resurrect-solve-intelligence-patent-ai-geo-expand.md
created: 2026-04-21T22:30:30+03:00
original_verdict_source: triage/triage-2026-04-14-solve-intelligence-patent-ai-geo-expand.md
---

# 01-intake

## Кейс
solve-intelligence-patent-ai-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-14-solve-intelligence-patent-ai-geo-expand.md

## Краткий контекст
Standalone legal/IP-кейс по patent AI для drafting, prosecution и claim charting. Требуется новая аналитика P3→P7, даже если исторически сигнал не проходил по LTV и считался недостаточно зрелым.

## Следующий шаг
Передать кейс в P3-demand-validation: проверить high-LTV buyer'ов, тяжесть локализации, сервисный слой и реалистичность GEO-EXPAND-сценария.

## Полный контекст из raw

# RESURRECT SIGNAL — solve-intelligence-patent-ai-geo-expand

## Meta
- source: triage/triage-2026-04-14-solve-intelligence-patent-ai-geo-expand.md
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
- pipeline/raw/raw-2026-04-14-solve-intelligence-patent-ai-geo-expand.md

## Классификация
новый сигнал, но кейс не открываем

## Решение
Не открывать новый кейс на этом этапе.

## Почему
- Подходящего открытого кейса в `pipeline/cases/` не найдено: текущие активные кейсы не покрывают вертикаль patent drafting / patent prosecution / claim charting как отдельную сервисную модель.
- Сигнал выглядит качественным, но по экономике не проходит порог Program 1: в raw-файле указан `ltv_signal: 800000-3000000 ₽ в год на клиента`, то есть примерно 67 000-250 000 руб. в месяц. Это заметно ниже порога `> 500 000 руб./мес.`.
- GEO-EXPAND логика присутствует, но локализация отмечена как `hard`: для России потребуются адаптация под процедуры Роспатента, работу патентных поверенных, русскоязычные формулы и локальные workflow в IP-операциях.
- В raw-файле нет достаточного подтверждения тяжёлого recurring service layer с высоким ежемесячным чеком, например managed implementation, интеграций в корпоративные R&D/IP-контуры или регулярного сопровождения больших патентных портфелей.

## Что сделано
- Новый кейс не создан.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Пометка для следующего шага
Вернуться к теме, если появятся дополнительные сигналы, подтверждающие хотя бы один из пунктов:
- enterprise LTV уверенно выше 500 000 руб. в месяц на клиента или контур;
- спрос со стороны крупных корпораций с большими IP-портфелями, а не только патентных фирм и отдельных специалистов;
- тяжёлый сервисный слой: внедрение, интеграции, защищённый контур, recurring сопровождение;
- признаки того, что patent AI в России или СНГ может стать операционным контуром, а не точечным инструментом.

## Вердикт
Сигнал интересный, но пока недостаточно сильный для открытия нового кейса в Program 1: LTV ниже порога, локализация тяжёлая, сервисная экономика не подтверждена.

```
