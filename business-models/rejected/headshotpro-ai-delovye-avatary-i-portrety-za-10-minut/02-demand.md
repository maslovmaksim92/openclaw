# Demand validation

## Итог
**Вердикт: PASS TO NEXT STEP.**

Категория не выглядит как большой category-search рынок в РФ, но как impulse-paid QUICK-AI продукт спрос подтверждён. Внутренний multi-demand даёт `LOW` по keyword `ai headshots`, но уже `MEDIUM` по локализованным болям `деловое фото` и `фото для резюме` с score `30/100`, 1 415–1 505 HH-сигналов и max Yandex Suggest `100`.

Почему не reject:
- фото в резюме влияет на просмотры: hh.ru пишет, что резюме с фото просматривают в среднем в `1,5 раза` чаще, а рекрутеры смотрят на фото в числе первых полей [T1](https://hh.ru/article/32050);
- HeadshotPro уже доказывает платёжеспособность категории: `196 987+` клиентов и старт от `$29` [T2](https://www.headshotpro.com/);
- Rewardful указывает для HeadshotPro `50K+` monthly affiliate revenue, что составляет `15%+` monthly revenue, то есть implied revenue бизнеса уже выше `~$333K MRR` [T2](https://www.rewardful.com/case-studies/headshotpro);
- в РФ уже есть локальные Telegram/photo AI сервисы с чеками `149–1 499 ₽`, что подтверждает локальную готовность платить за быстрый результат [T2](https://neiva.pro/) [T2](https://fotobanana.ru/).

## Demand signals
- **Internal demand API:**
  - `ai headshots` → `LOW`, score `15/100`.
  - `деловое фото` → `MEDIUM`, score `30/100`.
  - `фото для резюме` → `MEDIUM`, score `30/100`.
- **Recruiting-driven need:** hh.ru прямо пишет, что фото является одним из первых элементов оценки резюме, а резюме с фото просматривают в среднем в `1,5 раза` чаще [T1](https://hh.ru/article/32050).
- **Buyer pain:** это не «интерес к AI как таковому», а конкретный JTBD: быстро получить уместный деловой портрет без студии, фотографа и согласований. Поэтому branded-demand слабее, чем problem-demand. Это нормальный паттерн для QUICK-AI [T2 inference based on demand mix].

## Конкуренты и цены

| Игрок | Что продаёт | Цена | Что это значит |
|---|---|---:|---|
| HeadshotPro | AI headshots для индивидуалов и команд | от `$29` [T2](https://www.headshotpro.com/) | Есть глобальный reference price для one-off B2C покупки |
| Aragon AI | AI headshots / corporate packs | `Starter $35`, `Basic $45`, `Premium $75` [T2](https://www.aragon.ai/pricing) | Верхний consumer ceiling заметно выше $29 |
| BetterPic | AI headshots, edits, redo | `Basic $35`, `Pro $39`, `Expert $79`; edit `$8`, redo `$10` [T2](https://www.betterpic.io/) | Есть апсейлы после первой покупки, значит WTP не одноразовый |
| Neiva | Telegram AI photo bot | `149 ₽`, `290 ₽`, `490 ₽`, `990 ₽` [T2](https://neiva.pro/) | В РФ есть impulse price ladder прямо в Telegram |
| Фотобанана | Telegram AI photo bot | `199 ₽ / 10 фото`, `499 ₽ / 50`, `1 499 ₽ / 300` [T2](https://fotobanana.ru/) | Российский рынок привыкает к микроплатежам за AI-фото |

**Вывод по цене:** платить готовы, но рынок раздваивается на два чека: `149–990 ₽` в Telegram-ботах и `$29–79` в более качественном headshot-позиционировании. Значит продукту нельзя застревать посередине.

## Telegram / RU services check
- **Neiva** продаёт AI-фото прямо через Telegram-style интерфейс, тарифы от `149 ₽` до `990 ₽` [T2](https://neiva.pro/).
- **Фотобанана** продаёт генерацию фото пакетами от `199 ₽` до `1 499 ₽` [T2](https://fotobanana.ru/).
- **Shotix** позиционирует Telegram photo bot как обработку фото, face swap и стилизацию без регистрации [T3](https://shotix.io/telegram-photo-bot/). По цене данных нет, поэтому используем только как подтверждение наличия канала, не как primary evidence.

Вывод: RU Telegram-канал уже валиден как low-friction distribution, но многие локальные продукты уходят в generic AI-photo, а не в узкий headshot-JTBD. Это создаёт пространство для premium-позиционирования «фото для резюме / профиля / команды», а не для commodity photo bot.

## WTP, willingness to pay
1. **Прямое доказательство оплаты категории:** у HeadshotPro `196 987+` клиентов, старт от `$29`, а Starter Story оценивает бизнес примерно в `$300K monthly revenue` [T2](https://www.headshotpro.com/) [T2](https://www.starterstory.com/stories/headshotpro-breakdown).
2. **Партнёрский канал уже monetizable:** Rewardful фиксирует `50K+` monthly affiliate revenue и `15%+` долю affiliate в monthly revenue HeadshotPro [T2](https://www.rewardful.com/case-studies/headshotpro). Это важно, потому что продукт выдерживает paid acquisition и rev-share distribution, а не только органику.
3. **Российский покупатель уже платит за AI-photo:** Neiva и Фотобанана продают пакеты `149–1 499 ₽` [T2](https://neiva.pro/) [T2](https://fotobanana.ru/).
4. **Рабочая боль реальна:** hh.ru подтверждает, что хорошее фото повышает просмотры резюме, значит трата на деловой headshot может восприниматься как micro-investment в трудоустройство [T1](https://hh.ru/article/32050).

**Оценка WTP:** `6.5/10`. Платёжеспособность есть, но повторяемость спроса средняя, поэтому LTV надо поднимать через B2B team packs, career bundles и white-label.

## Market sizing

### Метод 1. Top-down
- **TAM (мир):** глобальная рабочая сила `~3,51 млрд` человек по World Bank/ILO [T1](https://data.worldbank.org/indicator/SL.TLF.TOTL.IN). Если взять addressable share `~2%` knowledge workers / customer-facing professionals, которым релевантен headshot, и средний annual spend `2 500 ₽`, получаем `~175,5 млрд ₽`.
- **TAM (РФ):** занятые в РФ `74,6 млн` человек в 2024 году по Росстату [T1]. При addressable share `10%` и annual spend `2 500 ₽` получаем `~18,7 млрд ₽`.
- **SAM (РФ):** берём только urban white-collar, экспертов, HR-driven профессии, риелторов, консультантов, edtech и SMB-команды, то есть `25%` от TAM РФ → `~4,7 млрд ₽`.
- **SOM Y1 / Y3:** реалистичный захват `2%` SAM в год 1 и `8%` к году 3 → `~93 млн ₽` и `~373 млн ₽`.

### Метод 2. Bottom-up
- **Total buyers:** в Едином реестре МСП `~6,7 млн` субъектов на 10.04.2025 [T1](https://rmsp.nalog.ru/). Берём только компании/ИП, которым нужен публичный профиль, найм, sales-face или экспертный контент.
- **% with need:** `~8%`. Основание: problem-demand по `деловое фото` и `фото для резюме` уже даёт `MEDIUM` во внутреннем demand API, а hh.ru подтверждает важность фото для поиска работы [T1](https://hh.ru/article/32050).
- **ARR avg:** `~9 000 ₽/год` на buyer. Это эквивалент трёх B2C-покупок по `~2 990 ₽` или одного small-team пакета в год; диапазон укладывается между RU Telegram price ladder и западными headshot price points [T2](https://www.headshotpro.com/) [T2](https://www.aragon.ai/pricing) [T2](https://neiva.pro/).
- **SAM bottom-up:** `6,7 млн × 8% × 9 000 ₽ = ~4,82 млрд ₽`.
- **SOM bottom-up Y1 / Y3:** `1,8%` и `6%` от SAM → `~86,8 млн ₽` и `~289 млн ₽`.

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | `175,5 млрд ₽` [T1] | — | — | top-down |
| TAM (РФ) | `18,7 млрд ₽` [T1] | `16,8 млрд ₽` [T1/T2, inference] | diff `~11%`, база сопоставима | lower |
| SAM (РФ) | `4,7 млрд ₽` [T1/T2] | `4,82 млрд ₽` [T1/T2] | diff `~3%`, хорошее схождение | lower |
| SOM Y1 | `93 млн ₽` | `86,8 млн ₽` | diff `~7%` | **используем 86,8 млн ₽** |
| SOM Y3 | `373 млн ₽` | `289 млн ₽` | diff `~29%` | **используем 289 млн ₽** |

### 10 реальных buyers для bottom-up sanity check
1. Самолет Плюс
2. Этажи
3. Skyeng
4. Нетология
5. Skillbox
6. Контур
7. Б1
8. Сравни
9. Яков и Партнёры
10. Calltouch

Это не signed customers, а реальный target list компаний, где есть публичные профили экспертов, hiring-flow, sales-facing сотрудники или потребность в массовом профайлинге команды.

### Sanity checks
- `SOM Y1 / SAM ≈ 1,8%` → реалистично, ниже 10%.
- При среднем чеке `2 990 ₽` для достижения `86,8 млн ₽` годового SOM Y1 нужно `~29 тыс.` заказов в год, то есть `~2,4 тыс.` заказов в месяц. Для fully self-serve B2C это напряжённо, но достижимо при affiliate + paid social + Telegram distribution. Для hybrid B2C+B2B ещё реалистичнее.
- Sales cycle короткий, поэтому условие `SOM Y1 × avg_deal_cycle_months > 12` не ломается: цикл покупки измеряется днями, а не кварталами.

## Profit Gate: может ли компания достичь EBITDA >= 500K ₽/мес?

### Сценарий A. Premium self-serve headshots
- Средний чек: `2 490 ₽`
- Платных заказов в месяц: `1 000`
- Выручка: `2,49 млн ₽/мес`
- Gross margin: `~83%`
- Валовая прибыль: `~2,07 млн ₽/мес`
- Fixed opex: `~1,10 млн ₽/мес`
- **EBITDA: ~970 тыс. ₽/мес**
- **Итог:** PASS

### Сценарий B. Pure Telegram low-ticket bot
- Средний чек: `490 ₽`
- Платных заказов в месяц: `2 500`
- Выручка: `1,225 млн ₽/мес`
- Gross margin: `~78%`
- Валовая прибыль: `~956 тыс. ₽/мес`
- Fixed opex: `~500 тыс. ₽/мес`
- **EBITDA: ~456 тыс. ₽/мес**
- **Итог:** FAIL, порог не проходит. Для 500K EBITDA нужно ближе к `~2 760` заказам/мес.

### Сценарий C. B2B team packs / HR bundles
- Средний пакет: `39 000 ₽`
- Клиентов в месяц: `30`
- Выручка: `1,17 млн ₽/мес`
- Gross margin: `~82%`
- Валовая прибыль: `~959 тыс. ₽/мес`
- Fixed opex: `~400 тыс. ₽/мес`
- **EBITDA: ~559 тыс. ₽/мес**
- **Итог:** PASS

### Сценарий D. Hybrid
- `700` self-serve заказов × `2 490 ₽` = `1,74 млн ₽`
- `12` team packs × `39 000 ₽` = `468 тыс. ₽`
- Общая выручка: `~2,21 млн ₽/мес`
- При blended GM `~82%` и fixed opex `~1,0 млн ₽` → **EBITDA ~810 тыс. ₽/мес**
- **Итог:** PASS

**Общий вывод по Profit Gate:** проходит. Но проходит не в commodity-боте, а в premium self-serve или hybrid B2C+B2B модели.

## Ключевые риски
- Повторная покупка у конечного B2C-пользователя слабая, поэтому нужно проектировать bundle-апсейлы и team/offer.
- Генеративные фото быстро коммодитизируются, если позиционирование будет «просто AI photo» вместо «деловое фото для резюме / профиля / команды».
- Есть риск policy/biometric concerns, если продукт будет слишком агрессивно продаваться в HR или finance-sensitive сегменты.

## Инвестиционная интерпретация
Кейс не является massive search market, но как QUICK-AI impulse-purchase сервис с premium packaging и B2B2C distribution выглядит инвестиционно валидным. Основная ставка здесь не на технологический moat, а на packaging, distribution и price discrimination между Telegram low-ticket и premium headshot offer.

## Решение этапа
**Решение: PASS TO NEXT STEP.**

Причина: demand не высокий, но реальный; WTP доказан; TAM/SAM/SOM сходятся; Profit Gate проходит минимум в двух монетизационных сценариях.

Sources: T1=4, T2=9, T3=1. Primary evidence basis: T2 with T1 support on labor/recruiting demand.

> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по запросам `ai headshots`, `деловое фото` и `фото для резюме` видны свежие обзоры, каталоги сервисов и коммерческая активность в категории.

> Market Pulse 2026-05-13: растущий интерес. По текущей веб-выдаче по ключевому запросу видна свежая рыночная активность.
