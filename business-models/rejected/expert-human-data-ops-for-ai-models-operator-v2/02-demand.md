---
stage: demand-validation
case: expert-human-data-ops-for-ai-models-operator-v2
date: 2026-04-19
analyst: branch-models-lead
verdict: REJECTED
confidence: medium
---

# 02-demand

## Executive summary

Кейс: сервис-оператор по expert human data ops для AI-моделей, то есть managed data labeling, human evaluation, RLHF/evals и dataset operations для корпоративных и frontier AI-команд.

Итог по спросу в РФ: **LOW**. По обязательному demand API ключи `data labeling`, `RLHF`, `разметка данных для ИИ`, `оценка LLM` все вернули `composite_demand=LOW`; самые сильные сигналы были у `оценка LLM` (`demand_score=26`, `hh_vacancies=328`) и `разметка данных для ИИ` (`demand_score=22`, `hh_vacancies=54`), но общий вывод API остаётся LOW [T1]. Источник: `http://172.18.0.1:9001/multi-demand`.

Для фонда это критично, потому что category в РФ есть, но она выглядит **узкой, проектной и с высокой трудоёмкостью**. В отличие от pure SaaS, human-data-ops масштабируется людьми и QA-слоем, поэтому при слабом локальном спросе пройти Profit Gate тяжело. После проверки трёх сценариев монетизации вывод: **Profit Gate FAIL**, устойчивый `EBITDA >= 500K ₽/мес` в РФ без выхода на внешний рынок выглядит малореалистично.

Следствие по правилу пайплайна: **DEMAND=LOW + Profit Gate FAIL => EARLY REJECT**.

## Demand signals

- `data labeling`: `LOW`, `demand_score=15`, `hh_vacancies=8`, `google_trends_ru=0` [T1].
- `RLHF`: `LOW`, `demand_score=18`, `hh_vacancies=23`, `google_trends_ru=1` [T1].
- `разметка данных для ИИ`: `LOW`, `demand_score=22`, `hh_vacancies=54`, `yandex_suggest=100` [T1].
- `оценка LLM`: `LOW`, `demand_score=26`, `hh_vacancies=328`, `yandex_suggest=100` [T1].

Интерпретация: в РФ есть **реальная профессиональная потребность** в evaluation/annotation для AI-команд, что видно по HH-сигналам [T1], но пока нет признаков широкого, регулярно закупаемого standalone-рынка managed human data ops. Спрос скорее концентрируется у ограниченного числа крупных AI-команд и интеграторов [T2].

Toloka прямо продаёт training data for AI agents and LLMs и позиционируется как поставщик human expert data [T2]. Это подтверждает существование категории, но одновременно показывает, что российский рынок уже занят сильным incumbent-игроком с международным наследием бренда [T2]. Источник: https://toloka.ai/ .

## Конкуренты и price anchors

Ниже даны реальные конкуренты и близкие заменители бюджета с публичными ценовыми ориентирами.

| Игрок | Что продаёт | Публичный price anchor | Источник | Вывод |
|---|---|---:|---|---|
| Prodigy | annotation tool для NLP/CV команд | **$390 one-time per license** [T2] | https://prodi.gy/#pricing | Дешёвый self-serve substitute, снижает willingness платить за managed-оператора у небольших команд |
| Label Studio Enterprise | data labeling platform | **от $149/seat/month** [T2] | https://sourceforge.net/software/product/Label-Studio/ | Seat-based альтернатива, выгоднее in-house команды при достаточном объёме |
| Datasaur | enterprise annotation platform | **от $5,000/year** [T2] | https://sourceforge.net/software/product/Datasaur/ | Для части use-cases платформа дешевле, чем постоянный managed-слой |
| Toloka | managed data + platform для AI/LLM | **цена публично не раскрыта** [T2] | https://toloka.ai/ | Крупный прямой конкурент в категории expert data ops |

Вывод по конкурентам: низкий ценовой floor у инструментов и сильный incumbent в managed-сегменте делают монетизацию нового оператора сложной. Чтобы выиграть, нужно или вертикальное domain expertise, или доступ к уникальному supply экспертов, или гарантии SLA/качества лучше рынка [T2].

## Telegram bots / services в РФ

Проверка обязательного demand API по всем ключам вернула `telegram.subscribers=0` [T1]. Это означает отсутствие заметного Telegram-distribution слоя в категории.

Ручная проверка тоже не даёт сильного сигнала: в РФ есть сервисы и комьюнити вокруг AI-разметки/краудсорсинга, но **не видно крупного Telegram-бота или Telegram-native сервиса**, который бы был каналом закупки expert human data ops [T2]. На практике продажи в этой категории идут через enterprise sales, тендеры, закрытые AI-команды и existing vendor relations, а не через Telegram [T2].

## WTP, willingness to pay

**WTP есть, но узкий и концентрированный.**

Подтверждения WTP:
1. HH-вакансии по `оценка LLM`, `RLHF` и `разметка данных для ИИ` показывают, что компании уже тратят деньги на внутренние команды разметки/evals, то есть бюджет на проблему существует [T1].
2. Платные инструменты Prodigy, Label Studio Enterprise и Datasaur показывают, что рынок готов платить хотя бы за tooling-слой [T2].
3. Toloka продаёт category-level managed service для AI/LLM, значит willingness платить за внешний human-data слой в принципе существует [T2].

Ограничения WTP:
1. Большая часть подтверждённого бюджета в РФ, вероятно, сидит у ограниченного списка крупных покупателей, а не у широкого SMB-рынка [T2].
2. При равной постановке задачи часть команд выберет in-house разметку + дешёвый tooling, а не внешний managed service [T2].
3. Для нового оператора без moat и бренда buyer risk высокий: утечки данных, качество аннотации, нестабильный throughput, высокая стоимость QA [T2/T3].

Итог: **WTP подтверждён как “точечный enterprise WTP”, но не как широкий и глубокий рынок**.

## Market sizing

**[LOW CONFIDENCE]** Рынок непрозрачен, поэтому считаю двумя способами и беру более консервативный результат.

### Top-down

1. Глобальный рынок data collection & labeling для AI оценён в **$3.6B в 2025** с ростом до **$17.1B к 2034** [T3]. Источник: Ciklum со ссылкой на рыночную аналитику, https://www.ciklum.com/resources/blog/understanding-ai-data-collection-and-labeling .
2. Более узкая категория data annotation tools оценивается примерно в **$1.02B в 2024** и растёт до **$3.64B к 2030** [T3]. Источник: Grand View Research, https://www.grandviewresearch.com/industry-analysis/data-annotation-tools-market-report .
3. Для РФ беру рабочую долю **1.0% global addressable spend** как консервативную верхнюю оценку, затем применяю discount на локальный enterprise-only сегмент из-за санкционного, procurement и privacy friction [T2/T3, analyst reconciliation].

Расчёт:
- TAM (мир): **≈ 297 млрд ₽/год** (беру $3.6B × 82.5 ₽/$) [T3]
- TAM (РФ): **≈ 2.97 млрд ₽/год** при доле 1.0% [T2/T3]
- SAM (РФ): **≈ 1.19 млрд ₽/год** при segment fit 40% только для enterprise AI teams и чувствительных use-cases [T1/T2/T3]
- SOM Y1: **≈ 35.7 млн ₽/год** при realistic capture 3% [T2/T3]
- SOM Y3: **≈ 119 млн ₽/год** при capture 10% [T2/T3]

### Bottom-up

Формула:
`Total buyers × % with need × ARR avg`

Допущения:
- Total buyers в РФ: **~120** компаний/команд, где реально может существовать регулярная потребность в expert annotation, RLHF, evals и sensitive data ops [T2]. Это крупные экосистемы, банки, телекомы, e-commerce, карты, voice/CX и AI-интеграторы.
- % with need: **35%** [T1/T2]. Основание: demand API показывает спрос, но он концентрирован, а не массов.
- ARR avg: **1.2 млн ₽/год** на клиента для retainer-модели или небольшого managed-пула [T2]. Это примерно 100 тыс. ₽/мес, уже выше self-serve tool альтернатив, но всё ещё слишком мало для жирной маржи.

Расчёт:
- SAM bottom-up = `120 × 35% × 1.2 млн ₽` = **50.4 млн ₽/год** [T1/T2]
- SOM bottom-up Y1 при capture 10% = **5.0 млн ₽/год** [T2]
- SOM bottom-up Y3 при capture 25% = **12.6 млн ₽/год** [T2]

### Reconciliation

Top-down даёт завышенную картину, потому что включает глобальный category-spend и не учитывает, что в РФ значительная часть спроса закрывается in-house или одним крупным incumbent-ом. Bottom-up лучше соответствует локальной реальности.

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 297 млрд ₽ [T3] | — | — | top-down |
| TAM (РФ) | 2.97 млрд ₽ [T2/T3] | 0.14-0.20 млрд ₽ [T1/T2, inferred from buyer base ceiling] | diff >3x, потому что top-down включает весь category spend, а bottom-up только реально достижимый локальный enterprise core | **lower** |
| SAM (РФ) | 1.19 млрд ₽ [T2/T3] | 50.4 млн ₽ [T1/T2] | diff >3x, top-down слишком широкий для нового игрока без moat | **50.4 млн ₽** |
| SOM Y1 | 35.7 млн ₽ | 5.0 млн ₽ | bottom-up реалистичнее | **5.0 млн ₽** |
| SOM Y3 | 119 млн ₽ | 12.6 млн ₽ | top-down не бьётся с buyer concentration | **12.6 млн ₽** |

### 10 реальных buyers для bottom-up sanity check

1. Яндекс / Yandex Cloud / YaGPT [T2]
2. Сбер / GigaChat [T2]
3. MTS AI [T2]
4. Т-Банк AI [T2]
5. VK / VK AI [T2]
6. Avito Tech [T2]
7. Ozon Tech [T2]
8. 2ГИС [T2]
9. ЦРТ / Speech Technology Center [T2]
10. BSS / Цифровые контакт-центры и voice AI интеграторы [T2]

Sanity check: даже если закрыть 5 клиентов в год со средним чеком 100 тыс. ₽/мес, годовая выручка будет лишь **6 млн ₽**, что намного ближе к bottom-up, чем к top-down [T2].

## Profit Gate: проверка всех сценариев монетизации

### Сценарий A. Managed expert annotation / eval service
- Средний контракт: **300 тыс. ₽/мес** [T2]
- Gross margin: **30%** [T2/T3], потому что большая часть выручки уходит экспертам, PM и QA
- Contribution на клиента: **90 тыс. ₽/мес**
- Фиксированные расходы: **~2.6 млн ₽/мес** для маленькой команды (founder + ops lead + QA lead + recruiter + sales + admin) [T2]
- Для `EBITDA 500K` нужно: `(2.6M + 0.5M) / 90K ≈ 35 клиентов`
- Вердикт: **FAIL**, для РФ это слишком много активных managed-клиентов

### Сценарий B. Tooling + managed QA hybrid
- ARPA: **120 тыс. ₽/мес** [T2]
- Gross margin: **70%** [T2]
- Contribution на клиента: **84 тыс. ₽/мес**
- Для `EBITDA 500K` нужно: `(2.6M + 0.5M) / 84K ≈ 37 клиентов`
- Вердикт: **FAIL**, при LOW demand и incumbent pressure недостижимо

### Сценарий C. Enterprise project / dedicated squad
- 1 проект: **1.5 млн ₽/мес** [T2]
- Gross margin: **25%** [T2/T3]
- Contribution на проект: **375 тыс. ₽/мес**
- Для `EBITDA 500K` нужно минимум **9 параллельных проекта**
- Вердикт: **FAIL**, это требует масштаба, бренда и delivery-машины уровня существующего лидера

### Итог по Profit Gate

**Profit Gate FAIL.** Во всех сценариях достижение `EBITDA >= 500K/мес` требует либо десятков клиентов, либо 9+ одновременных крупных проектов. Для локального российского рынка expert human data ops без явного moat это выглядит нереалистично [T2/T3].

## Stage verdict

**P4 verdict: REJECTED (early reject).**

Причины:
1. Обязательный demand API дал LOW по всем релевантным ключам [T1].
2. WTP существует, но у узкого числа enterprise buyers, а не у широкого рынка [T1/T2].
3. Конкуренты и substitutes ставят низкий ценовой потолок и давят маржу [T2].
4. Profit Gate не проходит ни в одном из основных сценариев монетизации [T2/T3].
5. Bottom-up SOM слишком мал для fund-level outcome без международной экспансии или сильного supply-side moat [T2].

## Sources

- Demand API: http://172.18.0.1:9001/multi-demand?keyword=data%20labeling [T1]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=RLHF [T1]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D1%80%D0%B0%D0%B7%D0%BC%D0%B5%D1%82%D0%BA%D0%B0%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85%20%D0%B4%D0%BB%D1%8F%20%D0%98%D0%98 [T1]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BE%D1%86%D0%B5%D0%BD%D0%BA%D0%B0%20LLM [T1]
- Toloka: https://toloka.ai/ [T2]
- Prodigy pricing: https://prodi.gy/#pricing [T2]
- Label Studio pricing listing: https://sourceforge.net/software/product/Label-Studio/ [T2]
- Datasaur pricing listing: https://sourceforge.net/software/product/Datasaur/ [T2]
- Ciklum market overview: https://www.ciklum.com/resources/blog/understanding-ai-data-collection-and-labeling [T3]
- Grand View Research data annotation tools: https://www.grandviewresearch.com/industry-analysis/data-annotation-tools-market-report [T3]

Sources: T1=4, T2=4, T3=2. Primary evidence basis: T1/T2.
