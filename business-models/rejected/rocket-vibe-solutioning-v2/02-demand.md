# Demand validation — Rocket Vibe

## Вывод
**Вердикт: REJECTED на этапе P4 Demand Validation.**

Категория AI-native solutioning для pre-sales, strategy, GTM и product scoping в РФ выглядит как реальная, но узкая enterprise/service-led боль, а не как широкий повторяемый software market. Mandatory demand endpoint по релевантным ключам стабильно возвращает **LOW**: `AI solutioning` — score 7, `product discovery` — score 22, `presales automation` — score 11, `solution consulting` — score 22. [Internal demand tool] При этом даже в лучших сценариях монетизации компания не набирает устойчивый **EBITDA >= 500 тыс. ₽/мес** без превращения в дорогой консалтинг. [T2 + inference]

## 1) Что именно валидируем
Rocket Vibe по брифу хочет продавать AI-native слой для discovery, solutioning, ICP/GTM definition, competitor intelligence и product scoping. По сути это гибрид между product discovery platform, pre-sales acceleration tool и strategy operator. [00-brief][T2]

## 2) Demand signals
- Internal endpoint `http://172.18.0.1:9001/multi-demand?keyword=AI%20solutioning` вернул **LOW / 7**: HH vacancies 53, Habr 2, Google Trends RU 0, Yandex Suggest 2. [Internal demand tool]
- `product discovery` вернул **LOW / 22**: HH vacancies 114, Yandex Suggest 100, но Google Trends RU 0, то есть рынок обсуждается в профессии, а не формирует массовый buying intent. [Internal demand tool]
- `presales automation` вернул **LOW / 11** при HH vacancies 257, что подтверждает наличие headcount-боли в presales/solution engineering, но пока не доказывает массовую закупку отдельного AI-продукта. [Internal demand tool]
- На hh.ru есть вакансии **Senior Solutions Architect / PreSale** с вилкой **300–500 тыс. ₽/мес** и **Менеджер presale / solution sale** с вилкой **250 тыс. ₽/мес**. Это подтверждает, что компании уже тратят значимый бюджет на ручной solutioning-слой. [T1]
- Вывод: спрос на функцию есть, но спрос на standalone AI-category в РФ пока **низкий и sales-led**, без сильного inbound/search tail. [T1][Internal demand tool]

## 3) Конкуренты и цены
Ниже не идеальные one-to-one клоны Rocket Vibe, а реальные substitute-конкуренты по бюджету discovery, scoping и product/prioritization workflows.

1. **Aha! Discovery / Aha! suite** — pricing page показывает планы от **$9, $39 и $59 за пользователя в месяц** в зависимости от продукта; discovery и product planning продаются как recurring SaaS. [T2]
2. **Miro** — pricing page и поисковый сниппет показывают **Starter $8/user/mo**, **Business $16/user/mo**, Enterprise custom; Miro прямо добавляет AI prototyping и insights для ранней проработки решений. [T2]
3. **Jira Product Discovery** — official pricing: **Free**, **Standard $10/creator/mo**, **Premium $25/creator/mo**, Enterprise custom. [T2]

### Что это значит
- Рынок уже платит за инструменты discovery/prioritization, но типичный software price anchor находится на уровне **$8–59 за seat** или low-hundreds per team, а не на уровне heavy retainer из коробки. [T2]
- Чтобы Rocket Vibe брать **150–300 тыс. ₽/мес**, ему нужен не просто tool, а measurable reduction of presales labor plus founder-grade strategic output. Это пока **инференс**, а не доказанный рыночный стандарт. [T2 + inference]

## 4) Telegram в РФ: боты и сервисы
Прямого сильного Telegram-native solutioning-бота в РФ по найденным данным не видно. Есть только adjacent services:
- **TGStat** продаёт аналитику Telegram-каналов, базу рекламы и market intelligence, тарифы начинаются **от 1 500 ₽/мес**. Это доказывает платёжеспособность за research/monitoring в Telegram, но не за strategy operator. [T2]
- **Telemetr** продаёт аналитику Telegram-каналов и рекламы, поисковый сниппет показывает тарифы **$15 / $25 / $55 в месяц**. [T2]
- **TGTerra** предлагает разработку Telegram-ботов **от 150 000 ₽**. Это ближе к кастомной automation-услуге, чем к масштабируемому solutioning SaaS. [T2]

### Вывод по Telegram
В RU Telegram есть оплата за аналитику и bot-development infrastructure, но нет убедительного сигнала, что рынок массово покупает Telegram-native AI strategy/solutioning operator. [T2 + inference]

## 5) Willingness to pay (WTP)
### Что подтверждено
- Компании уже платят **250–500 тыс. ₽/мес** сотрудникам presales / solutions architecture на hh.ru. Это сильный indirect proof наличия бюджета на саму функцию. [T1]
- Компании уже платят за tooling в discovery/insights: Aha!, Miro, Jira Product Discovery, TGStat, Telemetr. [T2]
- Но публичного доказательства, что российский buyer готов регулярно платить **>=150–300 тыс. ₽/мес** именно за AI-native solutioning layer без большой доли human services, не найдено. [T2]

### Вывод по WTP
**WTP подтверждён для функции, но слабо подтверждён для standalone-продукта.** Скорее всего, первая продаваемая конфигурация в РФ будет выглядеть как **service-heavy advisory + software assist**, а не как чистый SaaS. [T1][T2 + inference]

## 6) Market sizing
### Логика сегмента
Берём не весь IT-рынок, а узкий сегмент **AI-assisted discovery / pre-sales / solution consulting workflows** для крупных B2B-компаний, интеграторов, digital studios и enterprise product teams в РФ. Категория proxy-based, поэтому секция помечена как **[LOW CONFIDENCE]**. [LOW CONFIDENCE]

### Top-down
- TAdviser оценивал выручку **136 крупнейших IT-компаний РФ** в сегменте услуг за 2023 год в **470,6 млрд ₽**. Это не чистый рынок спроса, а supply-side proxy для IT consulting / implementation economy. [T2]
- Для discovery, scoping и presales-layer внутри этого пирога разумно брать лишь **0,4%** как узкую addressable долю. Тогда **TAM РФ ≈ 1,88 млрд ₽**. [T2 + inference]
- Из TAM оставляем **35%** под сегмент Rocket Vibe, где нужен именно повторяемый AI-assisted solutioning layer, а не любой консалтинг. Получаем **SAM ≈ 658 млн ₽**. [T2 + inference]
- Реалистичный capture: **Y1 = 3% SAM**, **Y3 = 10% SAM**. Тогда **SOM Y1 ≈ 19,7 млн ₽**, **SOM Y3 ≈ 65,8 млн ₽**. [inference]

### Bottom-up
- РБК 500 сообщает о **500 крупнейших компаниях РФ** с совокупной выручкой **142,3 трлн ₽** за 2024 год. Это хороший proxy для enterprise buyer universe. [T2]
- Отдельно TAdviser дал рейтинг **136 крупнейших IT-компаний** по услугам, то есть supplier-side buyers/partners, которые тоже могут покупать solutioning automation для pre-sales. [T2]
- Берём **636** потенциальных buyers в широком ICP: 500 крупнейших корпораций + 136 крупных IT-services игроков. [T2]
- Доля с реальной болью: **25%**, потому что отдельный AI solutioning layer нужен не всем, а прежде всего компаниям с длинным B2B sales cycle, кастомными внедрениями и частыми discovery-проектами. [T1][T2 + inference]
- Средний контракт: **2,4 млн ₽/год** или **200 тыс. ₽/мес**. Это соответствует hybrid-модели из software seat + expert review, но ещё не enterprise-consulting retainer. [T1][T2 + inference]
- Тогда **SAM_bottom_up = 636 × 25% × 2,4 млн ₽ = 381,6 млн ₽**.
- **SOM_bottom_up Y1 = 3% × 381,6 млн ₽ = 11,4 млн ₽**.
- **SOM_bottom_up Y3 = 10% × 381,6 млн ₽ = 38,2 млн ₽**.

### Таблица reconciliation
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | — | — | для категории нет чистого глобального T1 proxy | — |
| TAM (РФ) | 1,88 млрд ₽ [T2] | 1,53 млрд ₽ [T2] | diff ~1,23x, bottom-up уже режет buyer universe | lower |
| SAM (РФ) | 658 млн ₽ [T2 + inference] | 381,6 млн ₽ [T2 + inference] | diff ~1,72x, допустимо для proxy-category | lower |
| SOM Y1 | 19,7 млн ₽ | 11,4 млн ₽ | diff ~1,73x | **используем 11,4 млн ₽** |
| SOM Y3 | 65,8 млн ₽ | 38,2 млн ₽ | diff ~1,72x | **используем 38,2 млн ₽** |

### 10 реальных buyers для bottom-up
1. Сбер [T2]
2. Яндекс [T2]
3. VK [T2]
4. МТС [T2]
5. Ростелеком [T2]
6. Т-Банк [T2]
7. Альфа-Банк [T2]
8. Softline [T2]
9. КРОК [T2]
10. ЛАНИТ [T2]

### Sanity check
- SOM Y1 = 11,4 млн ₽ при среднем контракте 2,4 млн ₽/год означает около **5 клиентов** в первый год. [inference]
- При sales cycle **6–9 месяцев** это тяжело, но не невозможно; однако для компании это founder-led consulting motion, а не scalable SaaS flywheel. [T1][T2 + inference]
- SOM Y1 < 10% SAM, red flag overclaiming нет. [inference]

## 7) Profit Gate (EBITDA >= 500k ₽/мес)
Проверяю все основные сценарии монетизации.

### Сценарий A: self-serve workspace
- Цена: **49 тыс. ₽/мес**
- Клиентов: **20**
- Выручка: **0,98 млн ₽/мес**
- GM: **85%**
- Валовая прибыль: **0,83 млн ₽/мес**
- Даже при lean OPEX **1,6 млн ₽/мес** EBITDA будет **-0,77 млн ₽/мес**.
- **Gate: FAIL** [inference]

### Сценарий B: mid-market copilot + templates
- Цена: **149 тыс. ₽/мес**
- Клиентов: **12**
- Выручка: **1,79 млн ₽/мес**
- GM: **75%**
- Валовая прибыль: **1,34 млн ₽/мес**
- При OPEX **1,9 млн ₽/мес** EBITDA = **-0,56 млн ₽/мес**.
- **Gate: FAIL** [inference]

### Сценарий C: enterprise retainer
- Цена: **299 тыс. ₽/мес**
- Клиентов: **8**
- Выручка: **2,39 млн ₽/мес**
- GM: **60%**, потому что нужен human QA / strategy layer. [T1][T2 + inference]
- Валовая прибыль: **1,43 млн ₽/мес**
- При OPEX **2,1 млн ₽/мес** EBITDA = **-0,67 млн ₽/мес**.
- **Gate: FAIL** [inference]

### Сценарий D: advisory-heavy hybrid
- Цена: **600 тыс. ₽** за discovery-проект
- Объём: **4 проекта/мес**
- Выручка: **2,4 млн ₽/мес**
- GM: **40%**, потому что большая часть ценности создаётся экспертами, а не software. [T2 + inference]
- Валовая прибыль: **0,96 млн ₽/мес**
- При OPEX **2,0 млн ₽/мес** EBITDA = **-1,04 млн ₽/мес**.
- **Gate: FAIL** [inference]

### Итог по Profit Gate
**Profit Gate FAIL во всех проверенных сценариях.** Чтобы пройти порог, Rocket Vibe должен либо резко поднять ARPA без роста service-load, либо иметь сильный proprietary engine, который реально заменяет дорогой presales headcount. Публичных доказательств этого пока нет. [T1][T2 + inference]

## 8) Основные риски
1. **Category ambiguity risk**: buyer понимает проблему как consulting/discovery labor, а не как отдельную software category. [T1][T2]
2. **Service trap**: лучший early wedge почти неизбежно ведёт в кастомные исследования, scoping workshops и founder-heavy delivery. [T2 + inference]
3. **Weak standalone WTP**: есть бюджет на функцию, но нет сильного доказательства бюджета на продукт. [T1][T2]
4. **Long sales cycle**: ICP enterprise-heavy, а значит пилоты и procurement длинные. [T1][T2 + inference]

## 9) Инвестиционная интерпретация
Для фонда это выглядит не как будущая широкая software category, а как **AI-enabled boutique consulting layer**. Такой бизнес может быть полезным и денежным на уровне агентства, но текущих данных недостаточно, чтобы защитить software-like multiple, repeatability и EBITDA-скейлинг. [T2 + inference]

## Финальный вывод
- **Demand:** LOW по обязательному internal endpoint. [Internal demand tool]
- **Competitor pricing:** подтверждает бюджет на adjacent tooling, но mostly seat-based и недорогой. [T2]
- **Telegram/RU:** есть аналитика и bot-development services, но нет сильного локального solutioning-category signal. [T2]
- **WTP:** есть на функцию, слабый на standalone продукт. [T1][T2]
- **Profit Gate:** FAIL во всех сценариях. [inference]

**Решение на этапе demand validation: EARLY REJECT.**

## Источники
- Aha! pricing: https://www.aha.io/pricing [T2]
- Miro pricing: https://miro.com/pricing/ [T2]
- Jira Product Discovery pricing: https://www.atlassian.com/software/jira/product-discovery/pricing [T2]
- HH vacancy, Senior Solutions Architect / PreSale: https://hh.ru/vacancy/120257849 [T1]
- HH vacancy, менеджер presale / solution sale: https://hh.ru/vacancy/119925950 [T1]
- TAdviser, 136 крупнейших IT-компаний РФ в сегменте услуг: https://www.tadviser.ru/index.php/%D0%A1%D1%82%D0%B0%D1%82%D1%8C%D1%8F:136_%D0%BA%D1%80%D1%83%D0%BF%D0%BD%D0%B5%D0%B9%D1%88%D0%B8%D1%85_IT-%D0%BA%D0%BE%D0%BC%D0%BF%D0%B0%D0%BD%D0%B8%D0%B9_%D0%A0%D0%BE%D1%81%D1%81%D0%B8%D0%B8_%D0%B2_%D1%81%D0%B5%D0%B3%D0%BC%D0%B5%D0%BD%D1%82%D0%B5_%D1%83%D1%81%D0%BB%D1%83%D0%B3_2024 [T2]
- РБК 500, выручка крупнейших компаний РФ 142,3 трлн ₽: https://companies.rbc.ru/news/Hqu4bPNUUt/viruchka-krupnejshih-kompanij-rossii-vyirosla-do-142-trln-rublej/ [T2]
- TGStat pricing: https://tgstat.ru/analytics [T2]
- Telemetr tariffs: https://telemetr.me/en/tariffs [T2]
- TGTerra bot development: https://tgterra.ru/tg-bot [T2]

Sources: T1=2, T2=8, T3=0. Primary evidence basis: T2.
