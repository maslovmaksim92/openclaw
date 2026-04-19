# 02-demand — Demand Validation

## Кейс
0527-msk-sanas-geo-expand-v2, standalone demand-validation для Sanas / voice accent translation contact center wedge.

## Итог
**Статус: REJECTED (early reject).**

Категория показывает **LOW exact demand в РФ** по всем проверкам через mandatory demand API, а локальный Profit Gate не проходит ни в одном из трёх базовых monetization-сценариев. Для fund-level кейса это слишком узкий и слишком «импортный» wedge: глобально категория существует, но в российском контуре нет достаточного подтверждения, что можно собрать EBITDA >= 500 тыс. ₽/мес без чрезмерно оптимистичных допущений.

## 1. Demand data
Источник: `http://172.18.0.1:9001/multi-demand?keyword=accent%20translation%20contact%20center`

### Exact / adjacent checks
| Keyword | Composite demand | Demand score | Google Trends RU | hh.ru vacancies | Yandex suggest | Вывод |
|---|---|---:|---:|---:|---:|---|
| accent translation contact center | LOW | 0 | 1 | 0 | 2 | exact спрос в РФ практически отсутствует [T3] |
| voice accent translation | LOW | 0 | 0 | 0 | 2 | смежный поисковый спрос не сформирован [T3] |
| accent conversion call center | LOW | 0 | 0 | 0 | 2 | B2B intent в РФ не просматривается [T3] |
| Sanas accent translation | LOW | 0 | 1 | 0 | 2 | брендовый интерес в РФ минимален [T3] |

### Интерпретация
- По всем mandatory keyword-checks composite demand остаётся **LOW** [T3].
- Вакансий hh.ru по exact формулировкам **0**, значит рынок не показывает даже ранний локальный hiring-signal на категорию [T1/T3, потому что hh как источник Tier-1, но агрегат пришёл через internal API].
- Это не просто «новая категория без SEO», а скорее отсутствие локально сформированного pain-budget именно под accent conversion для contact center.

## 2. Реальные конкуренты и цены
Прямых публичных прайсов у Sanas нет, поэтому использую ближайшие коммерческие substitutes и adjacent competitors с открытыми тарифами.

| Конкурент | Категория | Публичная цена | Комментарий |
|---|---|---:|---|
| Krisp | AI accent conversion / noise cancellation | Pro **$8/user/month** при annual billing или **$16/user/month** monthly [T2] | Ближайший понятный ценовой якорь на voice-layer monetization |
| Wordly | AI speech translation / live interpretation | **от $1,690 за мероприятие** [T2] | Показывает willingness-to-pay за автоматизированный voice translation, но event use-case отличается |
| Wavel AI | AI dubbing / voice translation / localization | **$25 / $40 / $80 в месяц** по планам Lite / Pro / Business [T2] | Нижняя граница self-serve voice AI pricing |

### Вывод по конкурентному полю
- Платёжный якорь существует, но он находится либо в **global SaaS/self-serve**, либо в **event interpretation**, а не в российском B2B contact-center сегменте [T2].
- Для РФ это означает не готовый локальный budget line, а необходимость заново объяснять категорию и пилотировать её почти с нуля.

## 3. Telegram bots / services в RU
Проверка русскоязычного Telegram-контура показывает наличие только **consumer-grade transcription / translation bots**, но не enterprise-grade accent conversion для call center.

| Сервис | Что делает | Цена | Вывод |
|---|---|---:|---|
| Speakly | перевод аудио/видео в Telegram | **3 voice messages/day бесплатно**, далее платный доступ [T3] | consumer utility, не BPO/contact center tool |
| AudioScribeBot | транскрибация и перевод аудио | **5 минут бесплатно в день** [T3] | транскрибация, не accent translation |
| FindMiniBot | конвертация/обработка голосовых и видео | **10 минут бесплатно в день** [T3] | mass-market helper, не enterprise voice clarity stack |

### Вывод по RU Telegram
**Прямых Telegram-ботов/сервисов в РФ для accent-neutralization в contact center не найдено** [T3]. Это подтверждает слабую локальную сформированность категории, а не наличие скрытого SMB tailwind.

## 4. WTP, proof of willingness to pay
1. Компании уже платят за adjacent voice AI и translation tools, что подтверждают публичные цены Krisp, Wordly и Wavel AI [T2].
2. hh.ru показывает вакансии на англоязычную customer support функцию в РФ, то есть проблема multilingual support существует, но это ещё не доказательство отдельного бюджета на accent conversion [T1].
3. В российском контуре найден только consumer-level Telegram tooling, а не enterprise procurement pattern [T3].

### Вывод по WTP
**WTP подтверждён глобально, но не подтверждён в РФ именно для standalone accent translation layer**. Следовательно, fund-level demand для локального entry-point остаётся слабым.

## 5. Market sizing

### Метод и допущения
- Курс ЦБ РФ на 20.04.2026: **76.62 ₽/$** [T1].
- Глобальный контакт-центр software market: **$47.71 млрд в 2025** [T2].
- Российский рынок CCaaS: **3.5 млрд ₽ в 2025** [T2].
- Для accent translation / voice clarity layer беру **10% addressable share** от рынка CCaaS в РФ и **1.5%** от глобального contact-center software как узкий wedge [T2, аналитическое допущение].
- Для bottom-up беру **10 реальных buyer archetypes** и экстраполирую на **200 компаний** в РФ/СНГ с англоязычной support/sales функцией [T1/T2 + аналитическое допущение].
- Средний контракт: **1.8 млн ₽ ARR** (около 100 seats x ~$16 x 12 x 76.62 ₽, округлено вниз) [T1/T2].

### 10 реальных buyers для bottom-up
1. Aviasales [T1/T2]
2. Ostrovok [T1/T2]
3. Skyeng [T1/T2]
4. inDrive [T1/T2]
5. Tranio [T1/T2]
6. GMS Clinic [T1/T2]
7. Radisson Collection / hotel contact operations in RU [T2]
8. Яндекс Крауд [T1/T2]
9. Heroes of Support [T1/T2]
10. Bringo [T1/T2]

Это не доказанные клиенты Sanas, а **реальные target accounts / buyer archetypes** с международной или англоязычной клиентской коммуникацией.

### Расчёты
- **TAM (мир), top-down:** $47.71 млрд x 1.5% x 76.62 = **54.8 млрд ₽** [T1/T2]
- **TAM (РФ), top-down:** 3.5 млрд ₽ x 10% = **350 млн ₽** [T2]
- **TAM (РФ), bottom-up:** 200 buyers x 1.8 млн ₽ = **360 млн ₽** [T1/T2]
- **SAM (РФ), top-down:** 350 млн ₽ x 50% mid-market/enterprise export-heavy segment = **175 млн ₽** [T2]
- **SAM (РФ), bottom-up:** 120 buyers x 60% with acute need x 1.8 млн ₽ = **129.6 млн ₽** [T1/T2]
- **SOM Y1:** 3% capture = **5.25 млн ₽** top-down / **3.89 млн ₽** bottom-up
- **SOM Y3:** 8% capture = **14.0 млн ₽** top-down / **10.37 млн ₽** bottom-up

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | 54.8 млрд ₽ [T1/T2] | — | — | top-down |
| TAM (РФ) | 350 млн ₽ [T2] | 360 млн ₽ [T1/T2] | diff=3%, сходится | lower |
| SAM (РФ) | 175 млн ₽ [T2] | 129.6 млн ₽ [T1/T2] | diff=35%, acceptable: bottom-up строже | lower |
| SOM Y1 | 5.25 млн ₽ | 3.89 млн ₽ | diff=35% | **используем 3.89 млн ₽** |
| SOM Y3 | 14.0 млн ₽ | 10.37 млн ₽ | diff=35% | **используем 10.37 млн ₽** |

### Вывод по рынку
- Формально TAM/SAM не нулевые, но российский SAM остаётся **слишком узким** для fund-scale local wedge [T2].
- Предпочтительная оценка, это **нижняя граница** из bottom-up, потому что она опирается на реальные buyer archetypes и не завышает adoption [T1/T2].
- SOM Y1 меньше 10% SAM, значит модель не overclaiming, но абсолютный денежный объём всё равно слабый для venture-scale локального входа.

## 6. Profit Gate: EBITDA >= 500K/mo
Проверяю все базовые monetization-сценарии.

### Сценарий A. Self-serve seat model
- Цена: **1 490 ₽/seat/month** (локализованный price-point около нижней границы global tools) [T2]
- Валовая маржа: **75%**
- Fixed opex: **2.0 млн ₽/мес** (founder + sales + ML/support + infra) [спекуляция]
- Для EBITDA **500 тыс. ₽/мес** нужна валовая прибыль **2.5 млн ₽/мес**
- Нужно: 2.5 млн / (1 490 x 75%) = **около 2 238 seats**

**Вердикт:** FAIL. Для российского niche-demand это слишком большой объём seats.

### Сценарий B. Mid-market managed deployment
- Цена: **199 000 ₽/мес** [T2, derived from adjacent software + services basket]
- Валовая маржа: **60%**
- Fixed opex: **2.2 млн ₽/мес** [спекуляция]
- Для EBITDA **500 тыс. ₽/мес** нужна валовая прибыль **2.7 млн ₽/мес**
- Нужно: 2.7 млн / 119.4 тыс. = **около 23 аккаунтов**

**Вердикт:** FAIL. Для РФ получить 23 активных mid-market аккаунта в этой категории малореалистично.

### Сценарий C. Enterprise high-touch
- Цена: **450 000 ₽/мес** [T2, aggressive but still below heavy enterprise speech projects]
- Валовая маржа: **65%**
- Fixed opex: **3.0 млн ₽/мес** [спекуляция]
- Для EBITDA **500 тыс. ₽/мес** нужна валовая прибыль **3.5 млн ₽/мес**
- Нужно: 3.5 млн / 292.5 тыс. = **около 12 enterprise accounts**

**Вердикт:** FAIL. В локальном рынке не видно подтверждения, что 12 enterprise-клиентов готовы покупать отдельный accent-conversion layer.

### Общий вывод по Profit Gate
**Profit Gate FAIL.** Даже если WTP глобально существует, в РФ/СНГ достижение EBITDA >= 500 тыс. ₽/мес требует слишком большого количества seats или аккаунтов для рынка с LOW exact demand.

## 7. Финальный вывод по demand-stage
- Exact demand в РФ: **LOW** [T3]
- Реальные конкуренты с ценами: **есть**, но в основном global adjacent tools [T2]
- Telegram RU contour: **consumer bots only, enterprise wedge не найден** [T3]
- WTP: **глобально да, локально слабо** [T1/T2/T3]
- TAM/SAM/SOM: **ненулевые, но узкие для fund-scale локального entry** [T1/T2]
- Profit Gate: **FAIL во всех сценариях**

## Решение для пайплайна
**EARLY REJECT.**

Правило срабатывает полностью: **DEMAND = LOW** и **Profit Gate FAIL**, поэтому кейс нужно отклонить на Program 4 без перехода в economics stage.

## Источники
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=accent%20translation%20contact%20center
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=voice%20accent%20translation
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=accent%20conversion%20call%20center
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=Sanas%20accent%20translation
- Krisp pricing: https://krisp.ai/pricing/
- Wordly pricing: https://www.wordly.ai/pricing
- Wavel AI pricing: https://wavel.ai/pricing/
- ЦБ РФ, курсы валют: https://www.cbr.ru/currency_base/daily/
- Grand View Research, Contact Center Software Market: https://www.grandviewresearch.com/industry-analysis/contact-center-software-market-report
- РБК / ТМТ Консалтинг по рынку CCaaS РФ: https://companies.rbc.ru/news/UnyMlA7bP5/v-2025-godu-rossijskij-ryinok-oblachnyih-kontaktnyih-tsentrov-vyiros-do-35-mlrd-rublej/
- hh.ru search proxy: https://hh.ru/search/vacancy?text=%D0%B0%D0%BD%D0%B3%D0%BB%D0%B8%D0%B9%D1%81%D0%BA%D0%B8%D0%B9+customer+support
- Telegram bot directories: https://botcreators.ru/blog/best-telegram-bots-for-transcription/ , https://www.findmini.app/

Sources: T1=2, T2=6, T3=3. Primary evidence basis: T2.