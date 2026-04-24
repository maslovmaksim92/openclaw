---
stage: demand-validation
case: ai-yuridicheskiy-analiz-dogovorov-dlya-smb
date: 2026-04-24
analyst: branch-models-lead
sector: LEGALTECH
verdict: CONDITIONAL_PASS
confidence: medium
---

# 02-demand

## Кейс
AI-first юридический анализ и redline типовых договоров для SMB: первичный разбор, подсветка рисков, redline и комментарии за минуты, а финальный контроль остаётся у юриста.

## Итог
**Статус: CONDITIONAL PASS.**

- Спрос на exact-category в РФ не хайповый, а task-driven: `проверка договора онлайн` даёт **MEDIUM / 30**, `юрист по договорной работе` даёт **MEDIUM / 30**, а `анализ договора ИИ` остаётся **LOW / 26**. Это значит, что buyer платит за решение договорной рутины, а не за AI-лейбл. [T5]
- В willingness-to-pay есть доказуемый бюджет: Destra продаёт пакеты от **5 390 ₽** до **17 090 ₽** за кейс/сопровождение, Genie AI берёт **$75/мес** за Pro и **$600/мес** за Enterprise, Paxton AI стоит **$499/мес** или **$2 999/год** на пользователя. По курсу ЦБ на **24.04.2026** это примерно **5,6 тыс. ₽/мес**, **44,9 тыс. ₽/мес** и **37,4 тыс. ₽/мес** соответственно. [T1][T2]
- Локальный рынок Telegram уже занят каналами и консультационными сервисами, но специализированных RU Telegram-ботов именно под redline договоров почти не видно; demand API по запросу `проверка договора телеграм бот` показывает **LOW / 0**. Значит, Telegram скорее acquisition/support channel, а не самостоятельный moat. [T3][T5]
- Profit Gate проходит не в дешёвом self-serve SaaS, а в managed review / team subscription / outsourced legal ops. При цене **40–90 тыс. ₽ MRR** нужен портфель **6–13** клиентов, при цене **120–250 тыс. ₽ MRR** достаточно **2–5** клиентов, чтобы превысить **500 тыс. ₽ EBITDA в месяц** до штаб-квартиры компании. [T2][inference]

## 1. Спрос и сигналы рынка

### Demand API
- `проверка договора онлайн` → **MEDIUM**, `demand_score=30`, `hh_ru=662`, `yandex_suggest=100`. [T5]
- `анализ договора ИИ` → **LOW**, `demand_score=26`, `hh_ru=297`, `yandex_suggest=100`. [T5]
- `редлайн договора` → **LOW**, `demand_score=0`, `hh_ru=0`, `yandex_suggest=2`. [T5]
- `юрист по договорной работе` → **MEDIUM**, `demand_score=30`, `hh_ru=3386`, `yandex_suggest=100`. [T5]
- `проверка договора телеграм бот` → **LOW**, `demand_score=0`, `hh_ru=0`, `yandex_suggest=2`. [T5]

### Интерпретация
- Российский рынок ищет не “AI contract review”, а “проверка договора”, “договорная работа”, “согласование договора”, то есть workflow с понятным ROI. [T1][T5][inference]
- HH показывает не просто curiosity, а реальные бюджеты на договорную функцию: в выдаче есть вакансии **150 000 ₽**, **100 000–110 000 ₽**, **200 000–250 000 ₽** и другие, а работодатели включают White Hr, СДЭК, MDC Law и другие компании. Это прямой proxy на willingness-to-pay за замену/ускорение ручного труда. [T1]

## 2. Конкуренты и цены

| Конкурент | Формат | Публичная цена | Комментарий |
|---|---|---:|---|
| Destra Legal | онлайн-юрсервис / human-in-the-loop | 5 390 ₽, 8 990 ₽, 17 090 ₽ за пакет | Нижняя граница WTP на массовую удалённую юрпомощь в РФ. [T2] |
| Paxton AI | legal AI assistant | $499/польз./мес или $2 999/год | Upper-mid benchmark для solo/small legal teams. [T2] |
| Genie AI | contract drafting/review | $75/мес Pro, $600/мес Enterprise | Публичный ориентир для SMB и team-tier pricing. [T2] |
| Контур.Фокус Комплаенс | adjacent RU compliance review | 56 400 ₽, 193 200 ₽, 355 400 ₽ в год | Не прямой competitor, но доказывает готовность РФ-покупателя платить за document/compliance workflow. [T2] |

### Что это значит
- У рынка есть три ценовые полки: low-end human service до ~20 тыс. ₽ за кейс, SMB software примерно **5–45 тыс. ₽/мес**, и более тяжёлый enterprise/compliance слой от **190–355 тыс. ₽/год** и выше. [T2]
- Для нового AI-first игрока реалистичная стартовая монетизация в РФ, вероятно, лежит в зоне **40–90 тыс. ₽/мес** за команду или **8–20 тыс. ₽** за документный пакет с SLA. [T2][inference]

## 3. Telegram в РФ
- У **@pravovedru** есть Telegram-contact entrypoint, то есть legal inquiry через Telegram в РФ уже нормализован как канал обращения. [T3]
- У **DestraLegal** есть активный Telegram-канал, где сервис продвигает консультации и кейсы возвратов/претензий. [T3]
- Но evidence специализированных Telegram-ботов именно для AI-redline договоров почти нет; demand API по соответствующему запросу нулевой. [T3][T5]
- Вывод: Telegram годится как acquisition/support layer, но не подтверждает standalone bot-category. [T3][T5][inference]

## 4. WTP, proof of willingness to pay
1. **Прямой бюджет на юристов.** HH по запросу `юрист по договорной работе` показывает 3 386 вакансий, а в snippets видны вилки от **100 тыс. ₽** до **250 тыс. ₽** в месяц. Если продукт экономит хотя бы 0,3–0,5 FTE договорного юриста, у buyer появляется понятный бюджет в диапазоне **30–125 тыс. ₽/мес**. [T1][inference]
2. **Публичные software benchmarks.** Paxton и Genie уже монетизируют legal AI по подписке, а значит покупатель согласен платить не только за людей, но и за software seat / team workspace. [T2]
3. **Локальная service proof.** Destra показывает, что российский пользователь покупает удалённую юридическую услугу онлайн без офлайн-визита, то есть behavioural barrier уже снят. [T2]

## 5. Market sizing

### Метод и допущения
- Курс конвертации: официальный курс ЦБ РФ на **24.04.2026**, **1 USD = 74,8349 ₽**. [T1]
- База рынка РФ: в реестре ФНС на уровне РФ числится **6 947 425** субъектов МСП, из них **231 639** малых и **22 079** средних предприятий. [T1]
- Для адресуемого сегмента беру только малые и средние предприятия плюс небольшую долю микробизнеса с регулярным B2B-документооборотом; это консервативнее, чем считать весь реестр МСП. [T1][inference]
- Средний ARR для продукта: **180 000 ₽/год** на клиента, что соответствует **15 000 ₽/мес** на 1-2 seats либо эквиваленту 1-2 пакетов document review в месяц. Проверка: это выше low-end human consultation, но ниже Paxton-seat и сильно ниже full-service outsourced legal team. [T2][inference]

### Top-down
- Беру базу **253 718** компаний = все малые + средние предприятия МСП РФ. [T1]
- Предполагаю, что адресуемая доля для contract-review workflow составляет **25%** от этой базы, то есть компании с регулярным B2B contracting, наймом, поставками, маркетинговыми и подрядными договорами. Получаем **63 430** адресуемых компаний. [T1][inference]
- При среднем ARR **180 000 ₽/год** получаем **SAM_top_down ≈ 11,42 млрд ₽**. [T1][T2][inference]
- Для TAM РФ добавляю ещё верхний слой части микропредприятий: **500 000** микрокомпаний с повторяемым документооборотом × **120 000 ₽/год** ≈ **60,0 млрд ₽**, плюс small/medium block **45,7 млрд ₽**; итоговый **TAM РФ ≈ 105,7 млрд ₽**. [T1][T2][inference]
- Реалистичный захват: **Y1 = 1,5% SAM = 171 млн ₽**, **Y3 = 6% SAM = 685 млн ₽**. [inference]

### Bottom-up
- Беру **220 275** юрлиц малого и среднего бизнеса из реестра ФНС как более платёжеспособный ядро-сегмент. [T1]
- Доля с подтверждённой болью: **20%**. Обоснование, это консервативный слой компаний, где либо есть регулярная договорная работа, либо уже нанимают юристов/аутсорс по HH, либо интенсивно используют document workflows. [T1][T5][inference]
- Средний ARR: **180 000 ₽/год**. [T2][inference]
- **SAM_bottom_up = 220 275 × 20% × 180 000 ₽ ≈ 7,93 млрд ₽.** [T1][T2][inference]
- **SOM Y1 = 2% от SAM_bottom_up = 158,6 млн ₽.** [inference]
- **SOM Y3 = 8% от SAM_bottom_up = 634,4 млн ₽.** [inference]

### Таблица reconciliation
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 9,0-12,0 млрд $ для legal AI / contract AI category, спекулятивный внешний бенчмарк [T3] | — | Использую только как sanity check, не как основу модели | top-down |
| TAM (РФ) | 105,7 млрд ₽ [T1][T2][inference] | 39,6 млрд ₽ если взять 220 275 юрлиц МСБ × 100% need × 180 тыс. ₽ [T1][T2][inference] | diff=2,67x, допустимо; top-down включает часть микробизнеса, bottom-up ядро юрлиц | **lower** |
| SAM (РФ) | 11,42 млрд ₽ [T1][T2][inference] | 7,93 млрд ₽ [T1][T2][inference] | diff=1,44x, расхождение в норме | **7,93 млрд ₽** |
| SOM Y1 | 171 млн ₽ | 158,6 млн ₽ | diff=7,3% | **158,6 млн ₽** |
| SOM Y3 | 685 млн ₽ | 634,4 млн ₽ | diff=8,0% | **634,4 млн ₽** |

### 10 реальных buyers для bottom-up sanity check
Те же 10 targets, которые логично брать в GTM-10:
1. СДЭК [T1]
2. Самокат [T1]
3. Купер [T1]
4. Whoosh [T1]
5. Skyeng [T1]
6. 12 STOREEZ [T1]
7. Ригла [T1]
8. Лента [T1]
9. White Hr [T1]
10. MDC Law [T1]

### Sanity check
- При среднем чеке **180 тыс. ₽/год** SOM Y1 **158,6 млн ₽** означает около **881 клиентов** за год. Это много для founder-led complex sales, но достижимо только через self-serve + partner channel + templated workflows. [inference]
- Для pure outbound legal sales такой SOM Y1 агрессивен. Поэтому operational plan должен стартовать с меньшего revenue target, а Program gate оценивать по EBITDA-потенциалу, а не по первогоднему захвату полной SOM. [inference]

## 6. Profit Gate, все сценарии монетизации

### Сценарий A, self-serve seat SaaS
- Цена: **10–20 тыс. ₽/мес** на компанию.
- Валовая маржа высокая, но для EBITDA **500 тыс. ₽/мес** после команды и продаж нужно ориентировочно **70–120 клиентов**.
- Для РФ legal SMB go-to-market это долго и рискованно.
- **Вердикт: BORDERLINE / FAIL как стартовый wedge.** [T2][inference]

### Сценарий B, team subscription + monthly document quota
- Цена: **40–90 тыс. ₽/мес**.
- Для EBITDA **500 тыс. ₽/мес** достаточно примерно **6–13 активных клиентов** при lean-команде и высокой доле автоматизации.
- Это уже реалистично для boutique-to-productized модели.
- **Вердикт: PASS.** [T2][inference]

### Сценарий C, managed review / outsourced legal ops
- Цена: **120–250 тыс. ₽/мес** за постоянный поток документов, redline playbooks, SLA и эскалацию к юристу.
- Порог EBITDA можно пройти на **2–5 клиентах**.
- Лучшая стартовая конфигурация для РФ.
- **Вердикт: STRONG PASS.** [T2][inference]

### Сценарий D, one-off review / pay-per-document
- Цена: **8–25 тыс. ₽** за пакет или документ.
- Даёт быстрый вход, но плохо предсказуем по EBITDA без большого входящего потока.
- **Вердикт: PASS только как acquisition wedge, не как конечная модель.** [T2][inference]

## 7. Риски
- Exact-category search в РФ пока слабый, поэтому чистый “AI legal copilot” positioning не откроет спрос сам по себе. [T5]
- В low-end сегменте есть риск скатиться в дешёвую human service layer. [T2][inference]
- В enterprise-слое надо отдельно проверить хранение документов, локальный контур данных и ответственность за ошибки redline. [T3][inference]
- Telegram не выглядит product moat, только distribution add-on. [T3][T5]

## 8. Вывод для pipeline
**Кейс не отклонять.**

Почему:
1. спрос подтверждён как workflow pain, а не как vanity AI-category, [T1][T5]
2. willingness to pay доказан через зарплаты юристов и публичные цены конкурентов, [T1][T2]
3. Profit Gate проходит минимум в двух сценариях, team subscription и managed review, [T2][inference]
4. локальный Telegram-ландшафт пустоват именно в contract-AI, значит канал есть, но ниша ещё не переполнена. [T3][T5]

Что проверять дальше:
- реальную конверсию из pay-per-document в подписку,
- средний объём договоров на клиента в месяц,
- допустимый уровень ошибок AI-redline,
- требования к on-prem / private cloud для чувствительных документов,
- повторяемость продаж через партнёров, бухгалтеров, интеграторов и юрбутики.

## Источники
- [T1] ФНС, Единый реестр субъектов малого и среднего предпринимательства, статистика РФ: https://ofd.nalog.ru/statistics.html?level=2&fo_code=00&ssrf_code=00
- [T1] Банк России, официальный курс USD на 24.04.2026: https://www.cbr.ru/scripts/XML_daily.asp
- [T1] HH.ru, поисковая выдача по запросу `юрист по договорной работе`: https://hh.ru/search/vacancy?text=%D1%8E%D1%80%D0%B8%D1%81%D1%82+%D0%BF%D0%BE+%D0%B4%D0%BE%D0%B3%D0%BE%D0%B2%D0%BE%D1%80%D0%BD%D0%BE%D0%B9+%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B5
- [T2] Destra Legal, тарифы: https://destralegal.ru
- [T2] Paxton AI, pricing: https://www.paxton.ai/pricing
- [T2] Genie AI, pricing: https://www.genieai.co/pricing
- [T2] Контур.Фокус, тарифы Комплаенс: https://focus.kontur.ru/site/price-compliance
- [T3] Telegram contact Pravoved: https://t.me/pravovedru
- [T3] Telegram канал DestraLegal: https://t.me/s/destralegal
- [T5] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20%D0%B4%D0%BE%D0%B3%D0%BE%D0%B2%D0%BE%D1%80%D0%B0%20%D0%BE%D0%BD%D0%BB%D0%B0%D0%B9%D0%BD
- [T5] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7%20%D0%B4%D0%BE%D0%B3%D0%BE%D0%B2%D0%BE%D1%80%D0%B0%20%D0%98%D0%98
- [T5] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D1%80%D0%B5%D0%B4%D0%BB%D0%B0%D0%B9%D0%BD%20%D0%B4%D0%BE%D0%B3%D0%BE%D0%B2%D0%BE%D1%80%D0%B0
- [T5] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D1%8E%D1%80%D0%B8%D1%81%D1%82%20%D0%BF%D0%BE%20%D0%B4%D0%BE%D0%B3%D0%BE%D0%B2%D0%BE%D1%80%D0%BD%D0%BE%D0%B9%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B5
- [T5] Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20%D0%B4%D0%BE%D0%B3%D0%BE%D0%B2%D0%BE%D1%80%D0%B0%20%D1%82%D0%B5%D0%BB%D0%B5%D0%B3%D1%80%D0%B0%D0%BC%20%D0%B1%D0%BE%D1%82

Sources: T1=3, T2=4, T3=2. Primary evidence basis: T1.
