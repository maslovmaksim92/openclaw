# 02-demand — Lightyear geo expand v2

## Итог
**Вердикт по спросу: LOW.**
Кейс закрываю на P3 с ранним reject: в РФ есть бюджеты на корпоративную мобильную связь и смежный контроль расходов, но подтверждённого спроса именно на отдельный AI-native telecom procurement/TEM слой мало, а достижение **EBITDA 500 000 ₽/мес** выглядит нереалистичным при всех базовых сценариях монетизации.

## Demand signals
- `multi-demand` по запросу **telecom expense management** вернул **LOW / score 0**, hh.ru вакансий 0, Yandex suggest 2, Habr articles 2. [T2, internal tool via http://172.18.0.1:9001/multi-demand?keyword=telecom%20expense%20management]
- `multi-demand` по запросу **контроль расходов на связь** вернул **LOW / score 20**, hh.ru вакансий 2404, Yandex suggest 5. Это подтверждает боль вокруг расходов на связь, но не подтверждает отдельную категорию TEM-платформ. [T2, internal tool via http://172.18.0.1:9001/multi-demand?keyword=%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%BE%D0%BB%D1%8C%20%D1%80%D0%B0%D1%81%D1%85%D0%BE%D0%B4%D0%BE%D0%B2%20%D0%BD%D0%B0%20%D1%81%D0%B2%D1%8F%D0%B7%D1%8C]
- `multi-demand` по запросу **корпоративная мобильная связь учет** вернул **LOW / score 15**, hh.ru вакансий 3550. Это уже ближе к реальному рынку РФ, но категория всё равно выглядит сервисной/операторской, а не standalone SaaS. [T2, internal tool via http://172.18.0.1:9001/multi-demand?keyword=%D0%BA%D0%BE%D1%80%D0%BF%D0%BE%D1%80%D0%B0%D1%82%D0%B8%D0%B2%D0%BD%D0%B0%D1%8F%20%D0%BC%D0%BE%D0%B1%D0%B8%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F%20%D1%81%D0%B2%D1%8F%D0%B7%D1%8C%20%D1%83%D1%87%D0%B5%D1%82]
- На рынке РФ already bundled alternatives идут через операторов и UCaaS-поставщиков, что снижает пространство для отдельного TEM-vendor. [T2]

## Реальные конкуренты и цены
Ниже не 1:1 копии Lightyear, а **реальные substitutes**, за которые российский buyer уже платит.

1. **Mango Office, «Мобильная связь для бизнеса»** — от **1 960 ₽/мес** за пакет, далее тарифы выше по объёму. Это доказывает, что SMB/mid-market уже покупает bundled связь + кабинет + управление как один продукт. [T2, official pricing page: https://www.mango-office.ru/products/mobilnaya-svyaz/]
2. **t2 Бизнес, «Виртуальная АТС»** — от **350 ₽/мес**. Это более узкий substitute, но buyer платит за слой управления корпоративной телефонией поверх оператора. [T2, official pricing page: https://msk.t2.ru/business/telephony/virtualnaya-ats]
3. **билайн бизнес, тарифы ПроБизнес** — **410 ₽/мес**, **510 ₽/мес**, **1 020 ₽/мес**, премиум **20 000 ₽/мес**. Это показывает готовность платить за пакетированное управление корпоративной мобильной связью, а не за отдельный TEM-vendor. [T2, official pricing page: https://b2b.beeline.ru/products/mobile]

### Что это значит
- **WTP есть**, но она сфокусирована на **операторском пакете/кабинете**, а не на отдельном procurement/TEM stack. [T2]
- Для Lightyear это плохо: оператор уже владеет SIM, тарифом, биллингом и поддержкой, значит независимому слою сложнее забрать ARPU и маржу. [T2, inference]

## Telegram bots / services в РФ
- **t2 для бизнеса** имеет официальный Telegram-бот для уведомлений и управления. Это подтверждает, что российские операторы already extend service layer в Telegram. [T2, official page: https://msk.t2.ru/business/blog/news-list/telegram-bot]
- Отдельных заметных Telegram-ботов в РФ именно под TEM/procurement category не обнаружено; сигналов категории в Telegram мало. Это согласуется с LOW demand в internal tool. [T2]

## WTP (proof of willingness to pay)
1. Компании уже регулярно платят за корпоративную связь и сопутствующий control layer у операторов/UCaaS. [T2]
2. Цены публичны и recurring, значит бюджетная строка существует. [T2]
3. Но WTP направлена на **bundled telecom service**, а не на новый независимый AI procurement layer. Для Lightyear это **indirect WTP**, а не прямое подтверждение product pull. [T2, inference]

## Market sizing
**[LOW CONFIDENCE]** Категория TEM в РФ не раскрывается официально как отдельный рынок, поэтому считаю через cross-check top-down и bottom-up.

### Допущения
- Глобальный рынок telecom expense management: около **$4.2B**. [T3, market research roundup: https://www.openpr.com/news/4066758/telecom-expense-management-market-on-track-for-4-2-billion]
- Курс для расчёта: **90 ₽/$**. [T2, working assumption for model]
- В РФ база субъектов МСП около **6.4 млн**, из них средние предприятия около **0.3%**. Это даёт примерно **19 тыс.** средних компаний, к которым добавляется слой крупных enterprise. [T1+T2, ФНС SME registry plus analyst summaries]
- Для целевого сегмента Lightyear беру только distributed enterprise/mid-market с ощутимым telecom spend: **~3 000 компаний**. [T2, inference based on sector fit]
- Средний контракт для независимого control/procurement слоя в РФ: **600 000 ₽/год**. Это соответствует диапазону, где операторские и UCaaS-платежи уже заметны, но не enterprise-suite level. [T2, inferred from public tariffs above]

### Таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 378 млрд ₽ [T3] | — | — | top-down |
| TAM (РФ) | 1.13 млрд ₽ [T2/T3] | 1.80 млрд ₽ [T2] | diff=59%, top-down строже, т.к. считает только software/service overlay | lower |
| SAM (РФ) | 678 млн ₽ [T2/T3] | 360 млн ₽ [T2] | diff=1.9x, в пределах sanity | lower |
| SOM Y1 | 13.6 млн ₽ | 7.2 млн ₽ | diff=1.9x | **используем 7.2 млн ₽** |
| SOM Y3 | 67.8 млн ₽ | 36.0 млн ₽ | diff=1.9x | **используем 36.0 млн ₽** |

### Расчёт top-down
- Беру мировой TEM рынок **378 млрд ₽**. [T3]
- Доля РФ в enterprise telecom software/services для такого niche сегмента условно **0.3%** => **1.13 млрд ₽ TAM РФ**. [T2/T3, inference]
- Сегмент-fit для mid/large distributed buyers, где реально есть multi-SIM, procurement и invoice complexity, оцениваю в **60%** => **678 млн ₽ SAM РФ**. [T2, inference]
- Реалистичный захват: **2% Y1** и **10% Y3** => **13.6 млн ₽** и **67.8 млн ₽**. Это укладывается в правило SOM Y1 < 10% SAM. [T2]

### Расчёт bottom-up
- Total buyers: **3 000 компаний** целевого профиля в РФ. [T2, inference]
- % with need: **20%** реально чувствуют multi-operator / invoice / roaming / distributed-team pain => **600 компаний**. [T2, supported by hh/internal demand signals]
- ARR avg: **600 000 ₽/год**. [T2]
- **SAM_bottom_up = 600 × 600 000 = 360 млн ₽**.
- Реалистичный capture: **2% Y1** и **10% Y3** => **7.2 млн ₽** и **36 млн ₽**.

### 10 реальных buyers для bottom-up / GTM-10
1. X5 Group [T2]
2. Магнит [T2]
3. Лента [T2]
4. Ozon [T2]
5. Wildberries [T2]
6. Сбер [T2]
7. ВТБ [T2]
8. РЖД [T2]
9. Почта России [T2]
10. Ростелеком [T2]

Это компании с распределёнными командами, филиальной структурой, высоким количеством SIM/номеров, командировками и сложным invoice-flow. Но это **длинный enterprise sales cycle**, а не продукт с быстрым self-serve pull. [T2, inference]

## Profit gate: EBITDA >= 500 000 ₽/мес
Проверяю все базовые сценарии.

### Сценарий 1. SaaS per managed line
- Цена: **150 ₽/SIM/мес**. [T2, inferred market-friendly price]
- Gross revenue для 500 000 ₽ EBITDA при 2 FTE + founder + support и gross margin ~75% нужен примерно **1.1–1.3 млн ₽ MRR**. [T2, operating assumption]
- Это требует **7 300–8 700 SIM** под управлением.
- Для нового игрока без operator lock-in и без локальных интеграций с биллингом/документооборотом это слишком много для ранней РФ экспансии. **FAIL**. [T2, inference]

### Сценарий 2. Enterprise subscription
- Цена: **120 000 ₽/мес** на клиента. [T2, optimistic assumption]
- Для 500 000 ₽ EBITDA нужно примерно **9–10 клиентов** при lean team cost base. [T2]
- При LOW category demand и длинном sales cycle получить 9 enterprise logos быстро маловероятно. **FAIL**. [T2]

### Сценарий 3. Procurement / savings-share
- Комиссия: **10% от сэкономленного spend**. [T2, optimistic assumption]
- Чтобы получить **1.1 млн ₽+ revenue/month**, нужно обеспечивать клиентам **11 млн ₽+ подтверждённой ежемесячной экономии**. [T2]
- В РФ операторские сделки и скидки often relationship-driven; без статуса оператора/крупного реселлера это тяжело масштабировать. **FAIL**. [T2, inference]

### Сценарий 4. Managed service / audit
- Разовые аудиты и ручное сопровождение теоретически продаются, но это уже консалтинг, а не scalable product. Чтобы держать 500 000 ₽ EBITDA, нужен устойчивый поток новых enterprise проектов, которого текущие demand signals не показывают. **FAIL**. [T2]

## Вывод
- **Demand = LOW**.
- **Profit Gate = FAIL** по всем реалистичным сценариям.
- Следовательно, кейс подлежит **раннему REJECT** на этапе demand validation.

## Ссылки
- Internal demand tool: http://172.18.0.1:9001/multi-demand?keyword=telecom%20expense%20management
- Internal demand tool: http://172.18.0.1:9001/multi-demand?keyword=%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%BE%D0%BB%D1%8C%20%D1%80%D0%B0%D1%81%D1%85%D0%BE%D0%B4%D0%BE%D0%B2%20%D0%BD%D0%B0%20%D1%81%D0%B2%D1%8F%D0%B7%D1%8C
- Internal demand tool: http://172.18.0.1:9001/multi-demand?keyword=%D0%BA%D0%BE%D1%80%D0%BF%D0%BE%D1%80%D0%B0%D1%82%D0%B8%D0%B2%D0%BD%D0%B0%D1%8F%20%D0%BC%D0%BE%D0%B1%D0%B8%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F%20%D1%81%D0%B2%D1%8F%D0%B7%D1%8C%20%D1%83%D1%87%D0%B5%D1%82
- https://www.mango-office.ru/products/mobilnaya-svyaz/
- https://msk.t2.ru/business/telephony/virtualnaya-ats
- https://b2b.beeline.ru/products/mobile
- https://msk.t2.ru/business/blog/news-list/telegram-bot
- https://www.openpr.com/news/4066758/telecom-expense-management-market-on-track-for-4-2-billion

Sources: T1=1, T2=15, T3=1. Primary evidence basis: T2.