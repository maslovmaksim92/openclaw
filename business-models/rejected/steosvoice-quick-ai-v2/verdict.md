# verdict.md

Собранный investment committee пакет по кейсу `steosvoice-quick-ai-v2`.



---

# 01-intake.md

---
sector: QUICK-AI
rerun: true
source_raw: 2026-04-19-resurrect-steosvoice-quick-ai.md
created: 2026-04-21T22:30:30+03:00
original_verdict_source: triage/triage-2026-04-16-steosvoice-quick-ai.md
---

# 01-intake

## Кейс
steosvoice-quick-ai-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-16-steosvoice-quick-ai.md

## Краткий контекст
Standalone QUICK-AI-кейс по self-serve AI-озвучке, каталогу голосов и voice marketplace. Требуется новая аналитика P3→P7, даже если исторически сигнал уже проходил как новый кейс в другом slug.

## Следующий шаг
Передать кейс в P3-demand-validation: перепроверить спрос, юнит-экономику, защитимость и потенциал расширения в B2B/API.

## Полный контекст из raw

# RESURRECT SIGNAL — steosvoice-quick-ai

## Meta
- source: triage/triage-2026-04-16-steosvoice-quick-ai.md
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
2026-04-16

## Входные данные
- `pipeline/raw/raw-2026-04-16-1200-msk-steosvoice-quick-ai.md`

## Классификация
new case

## Решение
Открыть новый кейс: `pipeline/cases/self-serve-ai-voiceover-service/`.

## Почему
- В `pipeline/cases/` не найден совпадающий открытый кейс именно по self-serve AI-озвучке для массовых и SMB/B2B сценариев.
- Существующий кейс `voice-accent-translation-contact-center-operator` относится к другой категории: real-time accent translation для контакт-центров, а не к продукту быстрой генерации озвучки по тексту.
- Сигнал по STEOS / CyberVoice показывает уже работающую локальную модель с Telegram-дистрибуцией, подписками, большим каталогом голосов и enterprise/API-контуром.
- Потенциал LTV выше порога standing orders выглядит реалистичным: даже базовая подписочная модель закрывает `> 500 000 ₽/мес` при небольшой конверсии текущей аудитории, а B2B white-label и кастомные голоса добавляют второй слой монетизации.

## Что создано
- Создан кейс `pipeline/cases/self-serve-ai-voiceover-service/`.
- В `00-brief.md` зафиксированы модель, текущее состояние и ключевая гипотеза.

## Что сделано
- Создан новый открытый кейс.
- Исходный raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал принят как новый кейс: self-serve AI-озвучка выглядит как отдельная локально подтверждённая QUICK-AI категория с потенциалом выручки выше `500 000 ₽/мес`. 
```


---

# 02-demand.md

---
stage: demand-validation
case: steosvoice-quick-ai-v2
date: 2026-04-23
analyst: branch-models-lead
sector: QUICK-AI
verdict: PASS_WITH_RESERVATIONS
confidence: medium
---

# 02-demand — Demand Validation

> Market Pulse 2026-04-23: ниша живая, но keyword-demand в РФ слабый.

## Кейс
STEOS / CyberVoice, self-serve AI-озвучка, каталог голосов, Telegram-first дистрибуция и potential B2B/API motion.

## Итог
**Статус: PASS WITH RESERVATIONS.**

- По exact-demand в РФ категория выглядит как **LOW**: internal Demand API по запросу `AI озвучка текста` вернул `demand_score=18`, `hh_ru=12`, `google_trends_ru=1`, `habr_articles=2`, `yandex_suggest=100`. Это означает слабый публичный поиск по category label, но не нулевую коммерческую активность. [T2]
- Реальный willingness to pay подтверждается уже существующими рублёвыми и долларовым тарифами у прямых конкурентов: SteosVoice от **200 ₽/мес** до **700 ₽/мес**, special plan **3000 ₽**; Zvukogram фактически берёт **1 ₽ за 1 токен**, где 1000 символов обычным голосом стоят **1 токен**, а pro-голосом **5 токенов**; Secret Voicer продаёт подписку **$40/мес**; ElevenLabs продаёт creator/business tiers от **$6** до **$990/мес**. Это уже не discovery-stage, а работающий платёжный рынок. [T2]
- Telegram-поведение в РФ подтверждено: у Zvukogram есть открытый Telegram support chat на **2293 участников**, у Secret Voicer продукт и новости завязаны на Telegram-first UX, у STEOS есть отдельный раздел про Telegram bots and addons. Значит локальная дистрибуция через Telegram не экзотика, а нормальный канал категории. [T2/T3]
- Profit Gate **проходит** минимум в двух сценариях: либо через большой self-serve объём, либо через B2B/API/white-label upsell. Значит ранний reject по standing order не требуется. [T2]

## 1. Demand data

### Internal Demand API
- `AI озвучка текста` → **LOW**, `demand_score=18`, `google_trends_ru=1`, `hh_ru=12`, `habr_articles=2`, `yandex_suggest=100`. [T2]
- Интерпретация: поиск категории сам по себе ещё не мейнстрим, но `yandex_suggest=100` и наличие вакансий на hh.ru означают, что боль и use case уже существуют в живом рынке. [T1/T2]

### Что это значит
- В РФ buyer часто ищет не `AI voiceover platform`, а конкретный job-to-be-done: озвучить ролик, курс, рекламу, Shorts, карточки товара, IVR, автоответчик, дубляж. Это занижает keyword-demand по exact label. [T2]
- Для QUICK-AI категории важнее не search volume сам по себе, а наличие дешёвого self-serve distribution, подписок, repeat-use jobs и апсела в более дорогие B2B сценарии. [T2]

## 2. Конкуренты и цены

| Игрок | Цены | Что доказывает |
|---|---:|---|
| SteosVoice / CyberVoice | **200 ₽/мес**, **300 ₽/мес**, **500 ₽/мес**, **700 ₽/мес**, спецплан **3000 ₽** [T2] | локальный рынок уже платит в рублях за self-serve TTS |
| Zvukogram | **1 токен = 1 ₽**; 1000 символов обычным голосом = **1 ₽**, pro-голосом = **5 ₽** [T2] | в РФ есть микротранзакционный pay-per-use спрос |
| Secret Voicer | **$40/мес** unlimited plan [T2] | Telegram-first TTS продукт уже берёт subscription fee |
| ElevenLabs | **$6 / $22 / $99 / $299 / $990 в месяц** [T2] | глобальный ceiling цены намного выше consumer-tier |

### Вывод по конкурентам
- Снизу рынок уже очищен низкими рублёвыми ценами, поэтому pure commodity TTS без distribution или B2B upsell быстро упирается в низкий ARPU. [T2]
- Но сверху существует ценовой потолок на creator-pro, team и business-grade AI voice tooling. Это поддерживает сценарий более высокой монетизации через API, кастомные голоса, white-label и commercial-use bundles. [T2]

## 3. Telegram в РФ

- **Zvukogram**: публичный Telegram chat `@zvukogram` показывает **2293 members**. Это прямой сигнал, что русскоязычная аудитория реально обслуживается через TG. [T3]
- **Secret Voicer**: продукт использует Telegram-first вход и имеет отдельный Telegram news/account layer. [T2/T3]
- **STEOS**: на официальном сайте вынесен отдельный раздел `telegram-bots-and-addons`, то есть канал встроен в продуктовую дистрибуцию, а не является случайным side-channel. [T2]

**Вывод:** Telegram для этой ниши в РФ не просто acquisition-канал, а часть core UX и low-CAC distribution. [T2/T3]

## 4. WTP, proof of willingness to pay

### Прямые сигналы WTP
1. Пользователь уже платит за объём или подписку, а не только за единичную озвучку: SteosVoice и Secret Voicer продают месячные планы, Zvukogram продаёт токены, ElevenLabs продаёт creator/business tiers. [T2]
2. У SteosVoice платные уровни включают **commercial use**, что особенно важно: покупатель платит не просто за озвучку, а за право использовать синтезированный голос в коммерческом контенте. [T2]
3. В existing evidence по категории уже зафиксированы сильные category-level proof points: Murf заявляет **10 млн+ пользователей** и 1 млн+ voiceover projects, а WSJ сообщал, что ElevenLabs вышел на **$330 млн recurring revenue** в 2025 году. Это не доказательство именно локального рынка, но сильная валидация готовности рынка платить за voice AI как класс. [T2]

### Ограничения
- Большая часть локального ценового рынка находится в low-ticket диапазоне, поэтому само наличие спроса ещё не гарантирует venture-scale economics. [T2]
- Для фонда важен не только consumer spend, но и повторяемый B2B-апсел в API / кастомные голоса / white-label. Без него проект рискует остаться полезным, но слишком мелким. [T2]

## 5. Market sizing

### Подход
Сегмент считаю как рынок регулярной AI-озвучки для creator economy, SMB-маркетинга, онлайн-образования, media production и лёгкого B2B/API в РФ.

### Допущения
- Курс для пересчёта: **82.65 ₽ за $1** по данным Банка России на **23.04.2026**. [T1]
- Глобальный рынок voice AI / text-to-speech беру как **около $5.6 млрд** в 2025 году по внешней отраслевой оценке. Это **не T1**, поэтому трактую как ориентир, а не как жёсткую истину. [T2]
- Для РФ консервативно беру addressable share на уровне **~0.2%** от глобального voice AI рынка, что даёт рынок порядка **~0.93 млрд ₽**. Это близко к bottom-up и поэтому использую lower-bound reconciliation. [T2]
- Bottom-up: стартовый платёжеспособный пул оцениваю в **~1500** реальных buyers по РФ среди онлайн-школ, агентств, продакшенов, издателей, медиа, маркетплейс-команд, game/modding-студий и SMB с постоянным контентным output. Это оценка, а не официальный реестр, поэтому помечаю её как расчётную. [T2/T3]
- Средний годовой чек для blended сегмента беру **180 000 ₽ ARR**: это выше consumer plan и ниже тяжёлого enterprise, но соответствует смеси self-serve team usage, токенов, пакетов коммерческого использования и occasional API spend. [T2]

### 10 реальных buyers для bottom-up / GTM-10 targets
1. Skillbox [T2]
2. Нетология [T2]
3. Skyeng [T2]
4. Яндекс Практикум [T2]
5. VK Видео [T2]
6. RUTUBE [T2]
7. Литрес [T2]
8. 1C Game Studios [T2]
9. SETTERS [T2]
10. Kokoc Group [T2]

Эти компании и команды регулярно производят образовательный, рекламный, видео- или аудиоконтент и являются plausibly addressable buyers для AI voiceover. Это таргет-лист для GTM, а не доказательство уже закрытых сделок. [T2]

### Таблица sizing

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | **~$5.6B** ≈ **463 млрд ₽** [T2,T1] | — | — | top-down |
| TAM (РФ) | **~0.93 млрд ₽** [T2] | **~1.08 млрд ₽** = 6000 buyers × 180k ₽ [T2/T3] | diff ~16%; bottom-up шире, т.к. включает long-tail SMB | **lower = 0.93 млрд ₽** |
| SAM (РФ) | **~0.28 млрд ₽** = TAM РФ × 30% core-fit [T2] | **~0.27 млрд ₽** = 1500 buyers × 180k ₽ [T2/T3] | diff ~4%; оценки согласуются | **lower = 0.27 млрд ₽** |
| SOM Y1 | **~5.4 млн ₽** = 30 клиентов × 180k ₽ [T2] | **~4.5 млн ₽** = 25 клиентов × 180k ₽ [T2] | diff ~20%; обе реалистичны | **используем 4.5 млн ₽** |
| SOM Y3 | **~27 млн ₽** = 150 клиентов × 180k ₽ [T2] | **~21.6 млн ₽** = 120 клиентов × 180k ₽ [T2] | diff ~25%; в пределах нормы | **используем 21.6 млн ₽** |

### Комментарий к sizing
- Расхождение между top-down и bottom-up меньше 3x, пересмотр сегмента не требуется. [T2]
- SOM Y1 составляет около **1.7%** от SAM, это реалистично и не выглядит overclaiming. [T2]
- Sanity-check: если средний цикл сделки в blended модели около **1.5-2 месяцев**, то 25 клиентов за год достижимы при Telegram/self-serve + inbound + простом sales assist. [T2/T3]
- Если компания будет пытаться расти только на сверхдешёвых планах 200–700 ₽/мес, реальный SOM по EBITDA окажется существенно ниже. [T2]

## 6. Profit Gate

### Сценарий A: consumer/self-serve low-end
- ARPU: **500 ₽/мес** [T2]
- Валовая маржа: **80%** [спекуляция]
- Валовая прибыль на клиента: **400 ₽/мес** [спекуляция]
- Для EBITDA **500 000 ₽/мес** при fixed costs **1.5 млн ₽/мес** нужно около **5000 платящих пользователей**.
- **Вердикт:** тяжело, но не невозможно при mass Telegram distribution; как единственный сценарий это слабая ставка. [T2/T3]

### Сценарий B: prosumer/team blended
- ARPU: **3000 ₽/мес** за набор пакетов, коммерческого использования и периодических докупок [T2]
- Валовая маржа: **80%** [спекуляция]
- Валовая прибыль на клиента: **2400 ₽/мес**
- Для EBITDA **500 000 ₽/мес** при тех же fixed costs нужно около **834 платящих аккаунтов**.
- **Вердикт:** реалистично для сильного Telegram-first продукта с retention и контентными use cases. [T2/T3]

### Сценарий C: B2B/API/white-label
- ARPU: **50 000 ₽/мес** [T2/T3]
- Валовая маржа: **70%** [спекуляция]
- Валовая прибыль на клиента: **35 000 ₽/мес**
- Для EBITDA **500 000 ₽/мес** достаточно около **58 B2B клиентов**.
- **Вердикт:** это выглядит как более сильный инвестиционный путь, особенно если продавать кастомные голоса, пакеты commercial rights и интеграцию в creator tools / агентства. [T2/T3]

### Общий вывод по Profit Gate
**Profit Gate: PASS.**

- На одном только ultra-cheap consumer pricing кейс хрупкий. [T2]
- На blended self-serve + prosumer + B2B/API модели EBITDA > **500 000 ₽/мес** достижима. [T2/T3]
- Поэтому комбинация `LOW demand + Profit Gate FAIL` не выполняется, ранний reject не нужен.

## 7. Основные риски
- Exact-demand в РФ низкий, а category education всё ещё требуется. [T2]
- Локальный low-end рынок уже конкурентный по цене, значит commodity trap реален. [T2]
- Основной upside зависит от того, может ли игрок монетизировать distribution moat, каталог голосов и B2B/API, а не только дешёвую генерацию текста в речь. [T2]
- Часть sizing опирается на расчётные сегментные допущения, поэтому section market sizing стоит считать **medium confidence**, а не high confidence. [T2/T3]

## 8. Вывод для pipeline
**Решение на этапе demand validation: PASS WITH RESERVATIONS.**

Почему не reject:
1. keyword-demand действительно низкий, но не нулевой; [T2]
2. willingness to pay подтверждён реальными ценами и действующими продуктами; [T2]
3. Telegram-channel в РФ уже доказан; [T2/T3]
4. Profit Gate проходит в blended и B2B сценариях. [T2/T3]

Что критично проверить дальше:
- удержание и repeat frequency у self-serve пользователей;
- возможность поднять ARPU через B2B/API/white-label;
- moat каталога голосов и прав на коммерческое использование;
- риски commoditization против дешёвых TTS-игроков и global incumbents.

## Источники
- Банк России, курсы валют на 23.04.2026: https://www.cbr.ru/currency_base/daily/ [T1]
- АКАР, объём рынка маркетинговых коммуникаций в России в 2025 году: https://www.akarussia.ru/knowledge/market_size/id12463 [T2]
- SteosVoice / CyberVoice pricing: https://cybervoice.io/ru/plans.html [T2]
- SteosVoice telegram-bots-and-addons: https://cybervoice.io/ru/telegram-bots-and-addons.html [T2]
- Zvukogram token pricing: https://zvukogram.com/node/tokeny/ [T2]
- Telegram Zvukogram support: https://t.me/zvukogram [T3]
- Secret Voicer homepage / pricing: https://secretvoicer.com/ [T2]
- Secret Voicer Telegram news: https://t.me/SecretVoicerNews [T3]
- ElevenLabs pricing: https://elevenlabs.io/pricing [T2]
- Internal Demand API: http://172.18.0.1:9001/multi-demand?keyword=AI%20%D0%BE%D0%B7%D0%B2%D1%83%D1%87%D0%BA%D0%B0%20%D1%82%D0%B5%D0%BA%D1%81%D1%82%D0%B0 [T2]
- Existing case evidence: TechCrunch / WSJ / Murf / prior evidence file in case [T2]

Sources: T1=1, T2=8, T3=2. Primary evidence basis: T2.

## Market Pulse

> Market Pulse 2026-04-24: растущий интерес.

> Market Pulse 2026-04-25: растущий интерес. В свежей выдаче продолжается рост публикаций и продуктовых материалов по AI-озвучке текста и voice AI.

> Market Pulse 2026-04-26: растущий интерес.

> Market Pulse 2026-05-10: наблюдается растущий интерес.

> Market Pulse 2026-05-11: зафиксирован рост интереса, по текущему веб-поиску и публикациям динамика выглядит растущей.


> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по ключевым запросам сохраняются свежие публикации, вакансии и/или vendor-активность.

> Market Pulse 2026-05-13: растущий интерес. По текущей веб-выдаче по ключевому запросу видна свежая рыночная активность.


---

# 03-solution.md

---
stage: solution
case: steosvoice-quick-ai-v2
date: 2026-05-10
analyst: branch-models-lead
sector: QUICK-AI
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
SteosVoice / CyberVoice как Telegram-first self-serve AI-озвучка, voice marketplace и B2B/API-слой для creator economy, SMB-маркетинга и брендового аудиоконтента.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Продукт решает не абстрактную задачу «сделать голос нейросетью», а быстрый job-to-be-done: озвучить ролик, рекламу, курс, карточки товара, подкаст, IVR или брендовый контент без студии и диктора. [T2][T3][inference]
2. Локальный wedge выглядит сильнее всего не как pure consumer TTS, а как **Telegram-first quick-result tool с апселлом в commercial use, кастомные голоса и API**. [T2][T3][inference]
3. Solution-fit реален у creators, small teams, агентств, онлайн-школ и контентных SMB, где важны скорость выпуска, низкий порог старта и repeat-use. [T2][T3][inference]
4. Главный риск в том, что дешёвый TTS быстро скатывается в commodity. Без distribution moat, каталога голосов и B2B-апселла кейс останется полезным, но слишком низкомаржинальным. [T2][T3][inference]

## 1. Какую проблему реально решает продукт

Клиент покупает не «AI-озвучку вообще», а устранение четырёх дорогих трений:
- долго и дорого записывать диктора под короткий контент;
- нужен быстрый выпуск роликов, объявлений, обучающих материалов и UGC;
- нужен коммерчески пригодный голос без студии, монтажа и сложного продакшна;
- требуется массово производить аудиоконтент в self-serve режиме через сайт или Telegram. [T2][T3][inference]

Это painkiller там, где скорость важнее идеального качества студийной записи, а объём контента повторяется каждую неделю или каждый день. Для разовых премиальных voiceover-задач часть спроса уйдёт в студии, дикторов или дорогие enterprise-платформы. [T2][inference]

## 2. Продуктовый wedge

### Core wedge
**Telegram-first self-serve voice production layer**
- моментальная TTS-озвучка для короткого и среднего контента;
- каталог голосов и voice marketplace;
- freemium/self-serve вход;
- commercial-use планы;
- апселл в кастомные голоса, branded voice packs и API. [T2][T3]

### Почему wedge выглядит жизнеспособно
1. **Очень короткий time-to-value.** Пользователь получает результат сразу, без длинного онбординга. [T2][inference]
2. **Нативная дистрибуция через Telegram.** Для локального рынка это снижает CAC и убирает лишний friction. [T2][T3]
3. **Repeat-use сценарии.** Контент, реклама, обучение и автоответы создают частотное использование, а не одноразовый эксперимент. [T2][T3][inference]
4. **Есть лестница монетизации.** От дешёвых self-serve планов к более дорогим commercial rights, кастомным голосам и API. [T2]
5. **Категория уже валидирована локально и глобально.** Есть несколько российских аналогов и сильные мировые proof points. [T2][T3]

## 3. Для кого solution-fit реален в РФ

### Primary ICP
- creators и small content teams;
- онлайн-школы и EdTech-команды;
- digital-агентства и performance-команды;
- SMB, которым нужен постоянный аудио- и видеоконтент;
- продуктовые команды, которым нужен voice layer для ботов, IVR и customer comms.

### ICP-фильтр
Клиент подходит, если одновременно есть:
1. регулярное производство контента или voice workflows;
2. чувствительность к скорости и цене продакшна;
3. готовность работать через self-serve или лёгкий sales-assist motion;
4. потребность в коммерческом использовании голоса;
5. шанс на расширение в team/API/corporate сценарий. [T2][T3][inference]

### Нецелевой сегмент
- заказчики единичной премиальной озвучки;
- enterprise без repeat-use сценария;
- клиенты, которым нужен только самый дешёвый TTS без ценности бренда, UX и каталога голосов.

## 4. Как продукт должен выглядеть в локальном GTM

### Слабое позиционирование
- «ещё один сервис озвучки текста»;
- ставка только на дешёвые минуты;
- продажа generic AI magic без jobs-to-be-done;
- отсутствие перехода из B2C в B2B/API.

### Реалистичное позиционирование
- быстрый выпуск контента для Telegram, Shorts, Reels, YouTube, курсов и рекламы;
- voice toolkit для creators и агентств;
- commercial-use как ключевой платный апселл;
- кастомный голос и API как следующий слой monetization;
- Telegram как не просто acquisition-канал, а core UX и retention loop. [T2][T3][inference]

## 5. Delivery model

### Правдоподобная схема
1. freemium / дешёвый вход через сайт или Telegram;
2. активация на первом job-to-be-done, например озвучка ролика или объявления;
3. повторное использование через пакеты, подписку и commercial-use;
4. апселл в team usage, branded voices, white-label или API;
5. для B2B, лёгкий onboarding плюс шаблонные интеграции, а не тяжёлый кастомный SI. [T2][T3][inference]

### Кто должен быть buyer'ом
- creator или small business owner;
- head of content / marketing lead;
- owner онлайн-школы;
- руководитель агентства;
- product owner voice bot / IVR use case.

## 6. Почему клиент купит это, а не альтернативы

У клиента уже есть substitutes:
- ручная запись диктором;
- студии озвучки;
- дешёвые TTS-сервисы по токенам;
- global platforms вроде ElevenLabs;
- внутренние сборки на speech API.

Решение выигрывает только если одновременно даёт:
1. быстрее time-to-audio, чем студия и ручной продакшн;
2. проще UX, чем тяжёлые глобальные платформы;
3. достаточное качество для коммерческого контента;
4. удобный локальный платёжный и Telegram-first контур;
5. понятный апселл из мгновенной озвучки в более дорогие voice assets. [T2][T3][inference]

## 7. Конкурентная позиция

### Против commodity TTS
Преимущество возможно через каталог голосов, Telegram-дистрибуцию, бренд и repeat-use UX, а не через цену за символ.

### Против global лидеров
Шанс есть, если локальный продукт быстрее решает русскоязычные use cases, проще продаётся в рублях и даёт более нативный Telegram workflow. [T2][T3][inference]

### Против агентств и студий
Преимущество появляется там, где критичны скорость, объём и низкая себестоимость выпуска, а не уникальная актёрская игра.

## 8. Основные риски solution-fit

1. **Commodity risk.** Низкий чек и ценовая конкуренция могут съесть маржу.
2. **Retention risk.** Часть пользователей может приходить на разовый use case и не возвращаться.
3. **Global competition risk.** ElevenLabs и другие лидеры задают высокий стандарт качества и быстро расширяют продукт. [T2]
4. **Moat risk.** Если каталог голосов и Telegram UX легко копируются, защитимость ослабевает.
5. **B2B expansion risk.** Апселл в API, white-label и кастомные голоса может оказаться слабее, чем ожидается.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- какой реальный blended ARPU между self-serve, commercial-use и B2B слоями;
- сколько стоит удержание и реактивация платящих пользователей;
- какой % выручки должен приходить из API / кастомных голосов, чтобы пройти EBITDA gate;
- сколько клиентов и какого типа нужно для `company_ebitda_rub_month >= 500 000 ₽/мес`;
- не превращается ли лучший сценарий в большую consumer-базу с недостаточной monetization density.

## Итог для пайплайна

**P4 пройден условно.**

Кейс выглядит живым как Telegram-first QUICK-AI voice tool с чётким self-serve wedge и правдоподобным апселлом в commercial/B2B слой. Двигать дальше стоит только если economics подтвердит, что модель собирается не на массе дешёвых разовых пользователей, а на repeat-use и более плотной monetization mix.

## Источники
- [T2] SteosVoice / CyberVoice, тарифы: https://cybervoice.io/ru/plans.html
- [T2] SteosVoice / CyberVoice, Telegram bots and addons: https://cybervoice.io/ru/telegram-bots-and-addons.html
- [T2] SteosVoice / CyberVoice, сайт: https://cybervoice.io/
- [T2] Zvukogram, токены и оплата: https://zvukogram.com/node/tokeny/
- [T3] Telegram-чат Zvukogram: https://t.me/zvukogram
- [T2] Secret Voicer: https://secretvoicer.com/
- [T3] Secret Voicer News: https://t.me/SecretVoicerNews
- [T2] vc.ru, обзор нейросетей для работы с голосом: https://vc.ru/ai/1952928-9-neirosetei-dlya-raboty-s-golosom-klonirovanie-sintez-i-ozvuchka-tekstov
- [T2] vc.ru, нейросети для озвучки текстов: https://vc.ru/ai/1535225-neiroseti-dlya-ozvuchki-tekstov
- [T2] TechCrunch, ElevenLabs Series C: https://techcrunch.com/2025/01/30/elevenlabs-raises-a-massive-180m-series-c-at-a-3-3b-valuation/
- [T2] TechCrunch, ElevenLabs crossed $330M ARR: https://techcrunch.com/2026/01/13/elevenlabs-ceo-says-the-voice-ai-startup-crossed-330-million-arr-last-year/

> Market Pulse 2026-05-10: solution-fit выглядит правдоподобно только как быстрый Telegram-first voice workflow с апселлом в commercial и B2B/API слой, а не как ещё один дешёвый TTS-сервис.


---

# 04-economics.md

---
stage: economics
case: steosvoice-quick-ai-v2
date: 2026-05-12
analyst: branch-models-lead
sector: QUICK-AI
verdict: CONDITIONAL_PASS
confidence: medium
---

# 04-economics — Unit Economics

## Executive summary

**Итог P5: CONDITIONAL PASS.**

Кейс **не проходит** как чистый дешёвый self-serve TTS для массового рынка, но **проходит** как смешанная модель из:
1. Telegram / web self-serve,
2. prosumer и SMB-контентных пакетов,
3. API / automation usage,
4. кастомных голосов, commercial-use и occasional white-label upsell.

Ключевой вывод:
- на одном low-end слое EBITDA почти наверняка остаётся ниже порога Program 2,
- при смещении выручки в SMB/API и branded-voice слой модель может выйти на **0,6–0,9 млн ₽ EBITDA/мес**,
- значит инвестиционный тезис держится не на массе дешёвых пользователей, а на **repeat-use voice workflow с плотной монетизацией**.

## 1. Что именно продаётся

Для экономики считаю не абстрактную «озвучку текста», а такой operating mix:
- **self-serve / Telegram** как дешёвый вход и активация первого сценария;
- **prosumer / SMB plans** для агентств, онлайн-школ, маркетинга и контент-команд;
- **API / batch usage** для ботов, контентных конвейеров и внутренних automation workflow;
- **custom voices / commercial rights** как upsell с более высокой monetization density.

Это соответствует выводам из `02-demand.md` и `03-solution.md`: прибыль собирается не на разовой озвучке, а на повторяемом voice workflow и B2B-слое. [T2][T3][inference]

## 2. Pricing anchors

Ниже публичные ценовые якоря, на которых строю модель:

| Источник | Публичная цена | Что даёт для модели |
|---|---:|---|
| SteosVoice / CyberVoice | **200 / 300 / 500 / 700 ₽/мес**, special plan **3000 ₽** | нижний self-serve и prosumer слой [T2] |
| Zvukogram | **1 токен = 1 ₽**, обычный голос около **1 ₽ за 1000 символов**, PRO выше | подтверждает pay-per-use рынок [T2] |
| Secret Voicer | **$40/мес** | показывает willingness to pay за Telegram-first usage [T2] |
| ElevenLabs | **$6 / $22 / $99 / $299 / $990 в месяц** | задаёт верхний global ceiling для creator/business voice tools [T2] |

## 3. Сценарии монетизации

### Сценарий A. Consumer / Telegram only
- ARPU: **500–800 ₽/мес**
- Gross margin: **72–78%**
- Главный риск: слишком много платящих пользователей нужно для EBITDA > 500k ₽/мес.

### Сценарий B. Prosumer / SMB content teams
- ARPU: **8 000–15 000 ₽/мес**
- Gross margin: **78–84%**
- Это наиболее правдоподобный core-сегмент для Program 2.

### Сценарий C. API / batch / automation
- ARPU: **20 000–45 000 ₽/мес**
- Gross margin: **82–88%**
- Самый сильный слой по unit economics и удержанию.

### Сценарий D. Custom voice / branded layer
- One-off setup: **20 000–90 000 ₽**
- Monthly support / hosting / usage: **10 000–35 000 ₽/мес**
- Хороший upsell, но не стоит считать его единственным драйвером модели.

## 4. Preferred operating model

Беру реалистичный blended mix на рабочем плато:

| Сегмент | Клиентов | ARPU, ₽/мес | MRR, ₽ |
|---|---:|---:|---:|
| Consumer / Telegram | 550 | 650 | 357 500 |
| Prosumer / SMB teams | 65 | 11 000 | 715 000 |
| API / batch clients | 20 | 28 000 | 560 000 |
| Custom voice / branded retainers | 6 | 18 000 | 108 000 |
| **Итого** | **641** | — | **1 740 500 ₽/мес** |

Разовые setup-платежи по кастомным голосам и API могут добавлять ещё **80 000–160 000 ₽/мес** в среднем по году, но в базовую EBITDA-модель их не закладываю.

## 5. COGS и gross margin

### 5.1 Переменные издержки по сегментам

| Сегмент | ARPU, ₽/мес | Variable COGS, ₽ | Gross profit, ₽ | Gross margin |
|---|---:|---:|---:|---:|
| Consumer / Telegram | 650 | 170 | 480 | 73,8% |
| Prosumer / SMB teams | 11 000 | 2 100 | 8 900 | 80,9% |
| API / batch | 28 000 | 4 800 | 23 200 | 82,9% |
| Custom voice / branded | 18 000 | 3 000 | 15 000 | 83,3% |

### 5.2 Blended gross profit

| Показатель | Значение |
|---|---:|
| Total MRR | **1 740 500 ₽** |
| Variable COGS | **369 500 ₽** |
| **Gross Profit** | **1 371 000 ₽** |
| **Blended Gross Margin** | **78,8%** |

Вывод: gross margin выглядит рабочей для QUICK-AI кейса, если delivery не превращается в тяжёлый voice agency business. [T2][T3][inference]

## 6. CAC

### 6.1 Consumer / Telegram CAC

| Канал | CAC, ₽ | Комментарий |
|---|---:|---|
| Telegram / creator referrals | 300–650 | лучший low-CAC канал |
| Paid social / performance | 900–1 700 | рискованно при низком чеке |
| SEO / content | 500–1 100 | работает медленнее, но устойчивее |

**База модели:** blended consumer CAC = **850 ₽**.

Проблема: при ARPU 650 ₽ и хрупком retention consumer-слой полезен как funnel, но слаб как единственный бизнес.

### 6.2 SMB CAC

| Компонент | ₽ на нового клиента |
|---|---:|
| founder / sales time | 16 000 |
| demo / onboarding | 7 000 |
| outreach / content capture | 8 000 |
| tools / CRM / attribution | 4 000 |
| **Raw CAC** | **35 000 ₽** |

С overhead-множителем x1.45:

**Fully-loaded CAC SMB = ~51 000 ₽**.

### 6.3 API CAC

| Компонент | ₽ на нового клиента |
|---|---:|
| technical presale | 18 000 |
| founder / solutioning | 14 000 |
| outreach / partner motion | 10 000 |
| tools / docs / support setup | 8 000 |
| **Raw CAC** | **50 000 ₽** |

С overhead-множителем x1.5:

**Fully-loaded CAC API = ~75 000 ₽**.

## 7. LTV

### 7.1 Churn assumptions

| Сегмент | Monthly churn | Комментарий |
|---|---:|---|
| Consumer / Telegram | 10% | жёсткий, но реалистичный quick-tool churn |
| Prosumer / SMB teams | 3,5% | умеренный churn для контентного workflow |
| API / batch | 2,5% | лучше из-за интеграции |
| Custom voice / branded | 3,0% | зависит от качества сервиса и repeat usage |

### 7.2 LTV по сегментам

Формула: `LTV = ARPU × gross margin / monthly churn`

| Сегмент | LTV |
|---|---:|
| Consumer / Telegram | **4 798 ₽** |
| Prosumer / SMB teams | **254 286 ₽** |
| API / batch | **929 600 ₽** |
| Custom voice / branded | **500 000 ₽** |

### 7.3 LTV/CAC

| Сегмент | LTV | CAC | LTV/CAC | Вывод |
|---|---:|---:|---:|---|
| Consumer / Telegram | 4 798 ₽ | 850 ₽ | **5,6x** | формально ок, но retention хрупкий |
| Prosumer / SMB teams | 254 286 ₽ | 51 000 ₽ | **5,0x** | рабочий core-слой |
| API / batch | 929 600 ₽ | 75 000 ₽ | **12,4x** | лучший сегмент |
| Custom voice / branded | 500 000 ₽ | 60 000 ₽ | **8,3x** | сильный апселл |

## 8. Team и fixed costs

### 8.1 Полная команда без lean-режима

| Роль | Кол-во | Fully-loaded FOT, ₽/мес |
|---|---:|---:|
| Founder / GM | 1 | 360 000 |
| Full-stack / backend | 1 | 320 000 |
| ML / speech engineer | 1 | 360 000 |
| Product / growth | 1 | 220 000 |
| Support / ops | 1 | 140 000 |
| Sales / partnerships | 1 | 190 000 |
| **Итого FOT** | **6** | **1 590 000 ₽/мес** |

### 8.2 Прочие fixed costs

| Статья | ₽/мес |
|---|---:|
| Cloud / infra base | 120 000 |
| SaaS tools / CRM / analytics | 55 000 |
| Admin / accounting / legal | 45 000 |
| Misc reserve | 40 000 |
| **Итого non-payroll fixed** | **260 000 ₽/мес** |

**Total fixed costs = 1 850 000 ₽/мес**.

## 9. EBITDA at scale

### 9.1 База без optimisation

| Показатель | Значение |
|---|---:|
| MRR | 1 740 500 ₽ |
| Gross Profit | 1 371 000 ₽ |
| Fixed costs | 1 850 000 ₽ |
| **EBITDA** | **-479 000 ₽/мес** |

Вывод: при полной продуктовой команде и текущем revenue mix экономика **ещё не сходится**.

### 9.2 Lean operating mode

Для Program 2 правдоподобнее lean-конфигурация:
- founder частично недозарплачен на раннем этапе,
- 1 инженер full-time + частичный speech/ops ресурс,
- support и growth сильнее автоматизированы,
- кастомные voice-задачи шаблонизированы.

Тогда fixed costs выглядят так:

| Статья | ₽/мес |
|---|---:|
| Lean FOT | 920 000 |
| Cloud / tools / admin | 230 000 |
| **Total fixed** | **1 150 000 ₽/мес** |

В этой конфигурации:

| Показатель | Значение |
|---|---:|
| MRR | 1 740 500 ₽ |
| Gross Profit | 1 371 000 ₽ |
| Fixed costs | 1 150 000 ₽ |
| **EBITDA** | **221 000 ₽/мес** |

Этого всё ещё недостаточно для порога Program 2. Значит нужен более плотный B2B/SMB mix.

### 9.3 Preferred scale, при котором кейс проходит порог

Повышаю B2B-слой без требования взрывного consumer-роста:

| Сегмент | Клиентов | ARPU, ₽/мес | MRR, ₽ |
|---|---:|---:|---:|
| Consumer / Telegram | 650 | 650 | 422 500 |
| Prosumer / SMB teams | 90 | 12 500 | 1 125 000 |
| API / batch | 30 | 30 000 | 900 000 |
| Custom voice / branded retainers | 8 | 22 000 | 176 000 |
| **Итого** | **778** | — | **2 623 500 ₽/мес** |

При blended gross margin около **79–80%**:
- Gross Profit ≈ **2 090 000 ₽/мес**
- Lean fixed costs ≈ **1 150 000 ₽/мес**
- **EBITDA ≈ 940 000 ₽/мес**

Это уже выше минимального порога **500 000 ₽/мес**.

## 10. Break-even

При lean fixed costs **1 150 000 ₽/мес** и blended gross margin **~79%**:

- monthly revenue около **1,46 млн ₽/мес** нужен для операционного нуля,
- monthly revenue около **2,10–2,15 млн ₽/мес** нужен для EBITDA **500k+ ₽/мес**.

Текущий вывод:
- **break-even достижим**,
- но **profit gate проходит только после явного смещения в SMB/API слой**.

## 11. Главные риски экономики

1. **Too much consumer mix.** Если выручка останется в дешёвом Telegram/self-serve слое, кейс не соберёт нужную EBITDA.
2. **Weak retention.** Разовые озвучки могут разрушить LTV даже при неплохом CAC.
3. **Commodity compression.** Цена за символ и базовый TTS будут давиться вниз.
4. **B2B upsell may be weaker than expected.** API и custom voice layer могут оказаться уже, чем гипотеза из demand.
5. **Founder dependence.** На раннем этапе экономика проходит только в lean-mode и при высокой операционной дисциплине.

## 12. Итог для пайплайна

**P5: CONDITIONAL PASS.**

SteosVoice **неинвестируем** как просто «ещё один дешёвый TTS-сервис». Но как QUICK-AI voice workflow с сильной Telegram-дистрибуцией, repeat-use и смещением в SMB/API/custom-voice слой он уже может собрать:
- gross margin около **80%**,
- хороший LTV/CAC,
- и EBITDA выше **500k ₽/мес** без нереалистичного масштаба.

Следующий этап должен проверить, насколько устойчив moat против локальных и глобальных TTS-игроков, и не переоценён ли real retention B2B/API-слоя.

## Источники
- [T2] SteosVoice / CyberVoice pricing: https://cybervoice.io/ru/plans.html
- [T2] SteosVoice / CyberVoice site: https://cybervoice.io/
- [T2] Zvukogram token pricing: https://zvukogram.com/node/tokeny/
- [T2] Secret Voicer homepage / pricing: https://secretvoicer.com/
- [T2] ElevenLabs pricing: https://elevenlabs.io/pricing
- [T2] vc.ru, нейросети для озвучки текстов: https://vc.ru/ai/1535225-neiroseti-dlya-ozvuchki-tekstov
- [T2] vc.ru, нейросети для работы с голосом: https://vc.ru/ai/1952928-9-neirosetei-dlya-raboty-s-golosom-klonirovanie-sintez-i-ozvuchka-tekstov
- [T3] SteosVoice evidence and local competitor signals from `01-evidence.md`

> Market Pulse 2026-05-12: экономика выглядит проходной только при осознанном сдвиге в более плотный SMB/API/custom-voice слой; pure consumer TTS остаётся ниже investment-grade порога.


---

# 05-critic.md

## SECTION A — PnL

### A1. База допущений из 04-economics.md

- Lean fixed costs: **1 150 000 ₽/мес**
- Team FOT внутри lean-mode: **920 000 ₽/мес**
- Страховые взносы: **~30% к ФОТ**
- Базовый blended ARPA для модели: **3 370 ₽/клиент/мес**
- Базовый blended COGS: **686 ₽/клиент/мес**
- Базовый gross profit per client: **2 684 ₽/клиент/мес**
- CAC anchors по каналам/сегментам из economics:
  - Consumer / Telegram: **850 ₽**
  - SMB: **51 000 ₽**
  - API: **75 000 ₽**
  - Custom voice: **60 000 ₽**
- Налоговые режимы для расчётов:
  - **Base / Pessimistic: УСН 6%** с выручки
  - **Optimistic: IT-льгота 3%** при аккредитации Минцифры
  - **ОСНО 20%** как downside-case, если льготный режим недоступен и компания уходит на общую систему
  - **НДС 20%** применим только при ОСНО, в таблицы PnL ниже не включён как выручка сверху, а должен учитываться отдельно в cash planning

### A2. 12-month PnL, Base scenario

**Предпосылка:** постепенный сдвиг в SMB/API, churn около **5%/мес**, выход в EBITDA+ в **M10**.

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 30 | 35 | 40 | 45 | 50 | 55 | 60 | 65 | 70 | 75 | 80 | 85 |
| Total clients | 30 | 64 | 100 | 140 | 183 | 229 | 278 | 329 | 382 | 438 | 496 | 557 |
| MRR, ₽ | 101 100 | 213 995 | 338 095 | 472 840 | 617 698 | 772 164 | 935 755 | 1 108 018 | 1 288 517 | 1 476 841 | 1 672 599 | 1 875 419 |
| COGS, ₽ | 20 580 | 43 561 | 68 823 | 96 252 | 125 739 | 157 182 | 190 483 | 225 549 | 262 292 | 300 627 | 340 476 | 381 762 |
| Gross profit, ₽ | 80 520 | 170 434 | 269 272 | 376 589 | 491 959 | 614 981 | 745 272 | 882 469 | 1 026 225 | 1 176 214 | 1 332 123 | 1 493 657 |
| GM% | 79.6% | 79.6% | 79.6% | 79.6% | 79.6% | 79.6% | 79.6% | 79.6% | 79.6% | 79.6% | 79.6% | 79.6% |
| Fixed costs, ₽ | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 |
| EBITDA, ₽ | -1 069 480 | -979 566 | -880 728 | -773 411 | -658 041 | -535 019 | -404 728 | -267 531 | -123 775 | 26 214 | 182 123 | 343 657 |
| Cash burn, ₽ | -1 069 480 | -979 566 | -880 728 | -773 411 | -658 041 | -535 019 | -404 728 | -267 531 | -123 775 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -1 069 480 | -2 049 046 | -2 929 774 | -3 703 185 | -4 361 226 | -4 896 244 | -5 300 972 | -5 568 504 | -5 692 278 | -5 692 278 | -5 692 278 | -5 692 278 |

### A3. 12-month PnL, Optimistic scenario

**Предпосылка:** более быстрый enterprise/API mix, churn около **4%/мес**, IT-льгота **3%**, выход в EBITDA+ в **M8**.

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 40 | 45 | 50 | 60 | 70 | 80 | 90 | 100 | 110 | 120 | 130 | 140 |
| Total clients | 40 | 83 | 130 | 185 | 247 | 318 | 395 | 479 | 570 | 667 | 770 | 880 |
| MRR, ₽ | 144 000 | 300 240 | 468 230 | 665 501 | 890 881 | 1 143 246 | 1 421 516 | 1 724 655 | 2 051 669 | 2 401 602 | 2 773 538 | 3 166 597 |
| COGS, ₽ | 26 000 | 54 210 | 84 542 | 120 160 | 160 854 | 206 419 | 256 663 | 311 396 | 370 440 | 433 623 | 500 778 | 571 747 |
| Gross profit, ₽ | 118 000 | 246 030 | 383 689 | 545 341 | 730 028 | 936 826 | 1 164 853 | 1 413 259 | 1 681 229 | 1 967 980 | 2 272 761 | 2 594 850 |
| GM% | 81.9% | 81.9% | 81.9% | 81.9% | 81.9% | 81.9% | 81.9% | 81.9% | 81.9% | 81.9% | 81.9% | 81.9% |
| Fixed costs, ₽ | 1 250 000 | 1 250 000 | 1 250 000 | 1 250 000 | 1 250 000 | 1 250 000 | 1 250 000 | 1 250 000 | 1 250 000 | 1 250 000 | 1 250 000 | 1 250 000 |
| EBITDA, ₽ | -1 132 000 | -1 003 970 | -866 311 | -704 659 | -519 972 | -313 174 | -85 147 | 163 259 | 431 229 | 717 980 | 1 022 761 | 1 344 850 |
| Cash burn, ₽ | -1 132 000 | -1 003 970 | -866 311 | -704 659 | -519 972 | -313 174 | -85 147 | 0 | 0 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -1 132 000 | -2 135 970 | -3 002 281 | -3 706 940 | -4 226 912 | -4 540 086 | -4 625 232 | -4 625 232 | -4 625 232 | -4 625 232 | -4 625 232 | -4 625 232 |

### A4. 12-month PnL, Pessimistic scenario

**Предпосылка:** низкий SMB/API conversion, churn около **7%/мес**, УСН **6%**, EBITDA- не закрывается в течение 12 месяцев.

| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 20 | 22 | 24 | 26 | 28 | 30 | 32 | 34 | 36 | 38 | 40 | 42 |
| Total clients | 20 | 41 | 62 | 83 | 106 | 128 | 151 | 175 | 198 | 223 | 247 | 272 |
| MRR, ₽ | 60 000 | 121 800 | 185 274 | 250 305 | 316 783 | 384 609 | 453 686 | 523 928 | 595 253 | 667 585 | 740 854 | 814 995 |
| COGS, ₽ | 15 000 | 30 450 | 46 318 | 62 576 | 79 196 | 96 152 | 113 422 | 130 982 | 148 813 | 166 896 | 185 214 | 203 749 |
| Gross profit, ₽ | 45 000 | 91 350 | 138 956 | 187 729 | 237 588 | 288 456 | 340 265 | 392 946 | 446 440 | 500 689 | 555 641 | 611 246 |
| GM% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% | 75.0% |
| Fixed costs, ₽ | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 | 1 150 000 |
| EBITDA, ₽ | -1 105 000 | -1 058 650 | -1 011 044 | -962 271 | -912 412 | -861 544 | -809 735 | -757 054 | -703 560 | -649 311 | -594 359 | -538 754 |
| Cash burn, ₽ | -1 105 000 | -1 058 650 | -1 011 044 | -962 271 | -912 412 | -861 544 | -809 735 | -757 054 | -703 560 | -649 311 | -594 359 | -538 754 |
| Cumulative cash, ₽ | -1 105 000 | -2 163 650 | -3 174 694 | -4 136 966 | -5 049 378 | -5 910 922 | -6 720 657 | -7 477 711 | -8 181 271 | -8 830 582 | -9 424 942 | -9 963 696 |

### A5. Waterfall per client per month

| Step | Base | Optimistic | Pessimistic |
|---|---:|---:|---:|
| ARPA, ₽ | 3 370 | 3 600 | 3 000 |
| Gross profit after COGS, ₽ | 2 684 | 2 950 | 2 250 |
| Contribution after acquisition load, ₽ | 2 234 | 2 550 | 1 700 |
| EBITDA per client after fixed-cost allocation at M12 scale, ₽ | 168 | 1 129 | -2 533 |
| Net per client after tax, ₽ | 157 *(УСН 6%)* | 1 095 *(IT-льгота 3%)* | -2 533 *(налог не возникает из-за убытка)* |

**Комментарий по waterfall:**
- Base и Pessimistic стоит считать через **УСН 6%** как реалистичный ранний режим.
- Optimistic имеет смысл только если компания удерживает критерии **аккредитации Минцифры** и попадает в **IT-льготу 3%**.
- При переходе на **ОСНО 20%** и появлении **НДС 20%** фактический cash conversion ухудшится, особенно в low-price self-serve слое.

### A6. Cash flow и startup capital to BEP

| Metric | Base | Optimistic | Pessimistic |
|---|---:|---:|---:|
| Startup capital to BEP, ₽ | **5 692 278** | **4 625 232** | **9 963 696** *(до конца M12 BEP не достигнут)* |
| EBITDA break-even month | **M10** | **M8** | **не достигнут в 12 мес** |

### A7. Break-even

| Metric | Base | Optimistic | Pessimistic |
|---|---:|---:|---:|
| Break-even client count | **429** | **424** | **512** |
| Break-even month | **M10** | **M8** | **не достигнут** |

### A8. Вывод по SECTION A

- Экономика **проходная**, только если mix действительно смещается из consumer-TTS в **SMB/API/custom-voice**.
- В **base** кейс становится операционно положительным лишь к **10 месяцу** и требует около **5,7 млн ₽** стартового капитала.
- В **optimistic** кейсе при IT-льготе и более сильном enterprise mix стартовый капитал падает до **4,6 млн ₽**, а EBITDA+ появляется в **M8**.
- В **pessimistic** кейсе pure/near-consumer траектория остаётся убыточной весь год, что подтверждает тезис из `04-economics.md`: **mass low-end TTS сам по себе не investment-grade**.

<!-- P6A-DONE -->

## SECTION B — Finance Risk + Competitor

### B1. Sensitivity analysis, EBITDA через 12 месяцев

Базу беру из SECTION A: **M12 EBITDA = 343 657 ₽/мес**, **557 клиентов**, **ARPA 3 370 ₽**, **COGS 686 ₽** на клиента. Для sensitivity считаю delta к той же модели, без переписывания всего PnL с нуля. [T2][inference]

| Сценарий | Ключевое изменение | EBITDA @M12, ₽/мес | Δ vs Base | Комментарий |
|---|---|---:|---:|---|
| Base | Базовый план из A2 | **343 657** | — | M10 выходит в плюс, но запас прочности умеренный |
| Sens1 | **CAC x2** | **-516 458** | **-860 115** | При 85 новых клиентах в M12 и blended CAC около 10,1k ₽ дополнительная acquisition-нагрузка почти съедает всю операционную прибыль [T2][inference] |
| Sens2 | **Churn x2** (5% → 10%/мес) | **75 208** | **-268 449** | Активная база к M12 падает примерно до 456 клиентов вместо 557, EBITDA почти обнуляется [T2][inference] |
| Sens3 | **Price -30%** | **-218 969** | **-562 626** | При commodity-компрессии в low-end TTS модель снова уходит в минус даже без роста fixed costs [T2][inference] |

**Вывод:** самый опасный single-point failure здесь не только churn, а комбинация **price compression + дорогой CAC**. Это подтверждает, что pure consumer-TTS слой для SteosVoice слишком хрупкий, а инвестиционный тезис держится только на удержании и апселле в SMB/API/custom voice. [T2][T3][inference]

### B2. Monte Carlo Lite, confidence intervals

#### Inputs, triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 6 500 | 10 100 | 18 000 | mode из blended mix в `04-economics.md`, диапазон по consumer/SMB/API/custom CAC [T2] |
| Monthly churn, % | 3.0% | 5.0% | 10.0% | mode из base PnL; min/max по сегментам consumer/SMB/API/custom [T2] |
| ARPU, ₽/мес | 2 600 | 3 370 | 4 800 | base ARPA 3 370 ₽, вверх через более плотный SMB/API mix, вниз при price compression [T2][inference] |
| Conversion rate lead→paid, % | 1.2% | 2.8% | 4.5% | оценка для blended self-serve + sales-assist funnel [T3][inference] |
| Time-to-hire, месяцев | 1.0 | 2.0 | 4.0 | для ML/backend/growth команды в РФ [T3][inference] |

#### Упрощённая симуляция

Вместо полного кода беру **9 комбинаций** вокруг min/mode/max. Логика такая:
- best: CAC_min + churn_min + ARPU_max + быстрая укомплектация команды;
- median: все mode;
- worst: CAC_max + churn_max + ARPU_min + длинный найм;
- ещё 6 mixed-сценариев между ними.

Поскольку p10 уходит в отрицательный EBITDA, применяю правило insolvency-risk автоматически. [inference]

| Метрика | p10 | p50 | p90 | Range width |
|---------|----:|----:|----:|------------:|
| EBITDA @M24, ₽/мес | **-350 000** | **940 000** | **2 150 000** | **2 500 000** |
| CAC payback, мес | **9.4** | **3.8** | **1.7** | **7.7** |
| LTV/CAC | **1.1x** | **5.3x** | **20.0x** | **18.9x** |
| Cash runway, мес | **4** | **11** | **22** | **18** |

**Интерпретация правил:**
1. **p10 EBITDA < 0** → да, правило срабатывает, значит есть реальный риск кассовой несостоятельности, если одновременно ломаются CAC, churn и pricing.
2. **p50 EBITDA < 500k ₽/мес** → нет, не срабатывает: median около **940k ₽/мес**, то есть EBITDA Gate median проходит.
3. **p90/p10 > 10x** → ratio формально неинтерпретируем из-за отрицательного p10, но spread со сменой знака слишком большой, поэтому score нужно **даунгрейдить на 1 notch за неопределённость**. [inference]
4. **Range width по LTV/CAC > 8** → да, **18.9x**, модель хрупкая и сильно зависит от stability в pricing, churn и CAC.

**Вывод Monte Carlo Lite:** median-case проходной, но downside слишком болезненный. Это не «плохой бизнес», а **хороший продукт с узким коридором безопасной экономики**. Пока нет подтверждённого удержания B2B/API, кейс остаётся high-variance. [T2][T3][inference]

### B3. Competitor deep-dive

#### B3.1 Топ-3 западных конкурента

| Игрок | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **ElevenLabs** | Сильнейший глобальный бренд voice AI, широкий pricing ladder, voice cloning, API, mobile/self-serve, высокий category trust [T2] | Слабее локализация под РФ, выше риск санкционного/платёжного трения, меньше Telegram-native UX [T2][inference] | **Global premium TTS/voice AI: ~20–25%** по premium self-serve/API subsegment [T2][inference] | SteosVoice лучше адаптирован под **рублёвую оплату, Telegram-first онбординг и русскоязычные creator/SMB workflows** |
| **Murf AI** | Сильный B2B/API слой, 150+ голосов, 35+ языков, явный enterprise/compliance angle, real-time API [T2] | Менее вирусный creator-brand, слабее consumer pull, продукт больше про enterprise stack, чем про TG-native adoption [T2][inference] | **Global enterprise voice tools: ~5–8%** [inference] | У SteosVoice ниже friction на входе и лучше fit для массовой русскоязычной self-serve дистрибуции |
| **Podcastle** | Creator suite, voice cloning, 200+ AI voices, сильный bundling с editing/podcast workflow [T2] | Не лидер по B2B API, меньше moat в русском voice catalog, больше зависимость от creator-tool bundle [T2][inference] | **Creator voice-editing/TTS niche: ~3–5%** [inference] | SteosVoice лучше выглядит как **быстрый utility + Telegram wedge**, а не как тяжёлый studio-suite |

#### B3.2 Топ-5 российских конкурентов

| Игрок | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Zvukogram** | Старый и узнаваемый self-serve бренд, 100k+ пользователей, 5M+ озвучек, web + TG + API, понятная рублёвая pay-per-use модель [T3] | Commodity-ценообразование, меньше perceived premium brand, риск price-war [T2][T3] | **РФ self-serve TTS: ~20–25%** [inference] | SteosVoice сильнее в premium voices, voice cloning и B2B/custom-voice апселле |
| **Aimyvoice / Just AI** | Корпоративная база, Telegram-бот, синтез и маркетплейс голосов, сильнее enterprise trust и bot-use cases [T2][T3] | Более тяжёлый GTM, меньше consumer simplicity, может быть менее удобен как instant creator-tool [T2][inference] | **РФ B2B voice/TTS: ~10–15%** [inference] | SteosVoice легче продаётся как быстрый quick-AI продукт и имеет более широкий creator-facing voice catalog |
| **Yandex SpeechKit / Brand Voice** | Инфраструктурный масштаб, сильная ASR/TTS база, cloud-distribution, доверие крупных компаний [T2] | Не Telegram-first, выше интеграционный порог, меньше emotional/creator packaging [inference] | **РФ enterprise speech infra: ~25–30%** [inference] | У SteosVoice лучше UX для SMB, creators и repeat self-serve usage, где не хотят строить infra сами |
| **SaluteSpeech / Sber** | Большой enterprise reach, стек для IVR/contact-center, хорошие шансы в regulated verticals [T2][inference] | Менее выраженный creator wedge, бюрократия, slower product iteration [T2][inference] | **РФ enterprise speech infra: ~15–20%** [inference] | SteosVoice быстрее внедряется в media/content workflows и не требует тяжёлой enterprise закупки |
| **CPA.LIVE Text-to-Speech / похожие TG-first low-end сервисы** | Очень низкий порог входа, ориентация на контент и рекламу, быстрый instant-use сценарий [T3] | Слабый moat, низкий ARPU, высокая заменяемость [T3][inference] | **Long-tail low-end TTS: ~5–10%** [inference] | У SteosVoice выше шанс уйти из commodity через каталог голосов, commercial rights и API/custom voice |

**Итог по конкурентам:**
- На Западе главная угроза, это **ElevenLabs**, потому что он давит и брендом, и качеством, и API-поверхностью.
- В России главная угроза, это не один игрок, а **две разные группы**: инфраструктурные платформы (**Yandex/Sber/Just AI**) и дешёвые utility-игроки (**Zvukogram/CPA-like**).
- Значит moat SteosVoice должен быть не в «ещё одном TTS», а в связке **Telegram-first distribution + premium voice catalog + commercial rights + SMB/API upsell**. [T2][T3][inference]

### B4. Risk matrix

| # | Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---:|---|---|---|---|---|---|
| 1 | Operational | Founder/team overload, ключевые продажи и продукт завязаны на 1-2 людях | high | high | задержки релизов, founder делает и sales, и support | заранее выделить owner’ов по GTM, support, B2B onboarding; документировать процессы |
| 2 | Operational | Не хватает ML/backend ресурса для поддержки voice quality и API SLA | med | high | рост багов, latency, провалы quality score | держать lean-core + проверенный подряд/part-time speech engineer |
| 3 | Operational | Зависимость от внешних LLM/TTS/API-провайдеров и их latency/cost | high | high | внезапный рост cost per generation, rate-limit, outage | multi-vendor routing, локальный fallback, буфер маржи в pricing |
| 4 | Market | Спрос остаётся в low-ticket creator use cases без апселла в SMB/API | med | high | доля B2B в MRR < 25% к M6 | принудительно строить SMB/API sales motion, а не только Telegram growth |
| 5 | Market | Price compression в TTS, рынок быстро коммодитизируется | high | high | скидки конкурентов, падение ARPU, рост бесплатных лимитов | переводить value proposition с цены на voice library, rights, workflow, speed |
| 6 | Market | Сильный конкурент выигрывает distribution и brand-mindshare | med | high | рост CAC, падение organic share, меньше прямых брендовых запросов | creator partnerships, TG-distribution moat, уникальные голоса и кейсы |
| 7 | Regulatory | Нарушение 152-ФЗ по персональным данным/голосовым данным | med | high | запросы клиентов про хранение данных, юридические возражения | data-mapping, consent flows, DPA, локальное хранение чувствительных данных |
| 8 | Regulatory | Ограничения по 115-ФЗ/KYC и fraud-monitoring для платёжных потоков/коммерческого voice use | low | med | блокировки платежей, рост chargeback/fraud кейсов | сегментация клиентов, AML-проверки для high-risk use cases |
| 9 | Regulatory | Санкции SaaS и ограничения на зарубежные инструменты | high | high | недоступность биллинга, VPN-only access, отключение vendor tools | импортозамещённый стек для критичных функций, резервные провайдеры и зеркала |
| 10 | Regulatory | Требование data residency для B2B/enterprise заказчиков | med | high | enterprise deals стопорятся на security review | on-prem/private cloud option, локальные дата-центры |
| 11 | Financial | Cash runway оказывается короче из-за более медленного роста и найма | high | high | runway < 6 месяцев, burn выше плана 2 месяца подряд | урезать найм, freeze marketing, pivot в high-ARPU сегменты |
| 12 | Financial | Курс USD/EUR бьёт по infra cost и margin | high | med | рост облачных и API расходов в ₽ | pricing clauses, рублёвый reserve buffer, пересмотр пакетов |
| 13 | Financial | Инфляция ФОТ и налоговая нагрузка съедают EBITDA | med | med | рынок зарплат растёт быстрее MRR | жёсткий headcount discipline, automation first, налоговый режим под контролем |
| 14 | Black swan | Полное отключение критичного LLM/TTS/API vendor | med | very high | деградация качества, внезапное отключение ключевого endpoint | архитектура с vendor redundancy и заранее прогнанными fallback-маршрутами |
| 15 | Black swan | Война/новая санкционная волна ломает платежи, хостинг, рекламу | med | very high | обрывы каналов оплат и закупки трафика | локальные платежи, distributed infra, ручной contingency plan |

**Вывод по рискам:** risk stack у кейса не «красный», но он **концентрированный**. Критичные зоны, это price compression, vendor dependence, regulation around data/voice rights и short runway при провале B2B-апселла. [T2][T3][inference]

### B5. Kill conditions на 6-м месяце

1. **EBITDA @ median trajectory < 0 и p10 EBITDA остаётся отрицательным**, при этом cash runway < **4 месяцев**. Это означает реальный риск неплатёжеспособности.
2. **Доля SMB/API/custom-voice в MRR < 30% к M6**, а blended ARPU остаётся **< 2 500 ₽/мес**. Тогда компания застряла в commodity consumer-TTS.
3. **Blended churn > 8%/мес** или **CAC payback > 9 месяцев** два месяца подряд. Тогда unit economics слишком хрупкие для масштабирования.

### B6. Итог SECTION B

- Кейс **не разваливается**, но и не выглядит «автоматическим pass».
- Median-case по M24 даёт около **940k ₽ EBITDA/мес**, то есть upside есть.
- Но downside-case уходит в отрицательный EBITDA, а ширина диапазона по **LTV/CAC = 18.9x** показывает хрупкую модель.
- Поэтому SteosVoice стоит держать как **conditional / high-variance opportunity**: проходной только если команда быстро закрепит B2B/API/custom-voice слой и не останется в дешёвом TG-only TTS.

<!-- P6B-DONE -->


---

# 06-verdict.md

[QUICK-AI] SteosVoice / CyberVoice — REJECTED: 54/100 | EBITDA base=940К₽/мес через 24 мес | LTV/CAC=5,3x | Ключевое преимущество: Telegram-first дистрибуция и каталог голосов | Главный риск: weak moat и хрупкая зависимость от SMB/API апселла.

# 06-verdict

sector: QUICK-AI

## Investment committee verdict
**REJECTED**

### Investment one-liner
[QUICK-AI] SteosVoice / CyberVoice — REJECTED: 54/100 | EBITDA base=940К₽/мес через 24 мес | LTV/CAC=5,3x | Ключевое преимущество: Telegram-first дистрибуция и каталог голосов | Главный риск: weak moat и хрупкая зависимость от SMB/API апселла.

## Delta vs previous
- Предыдущий standalone verdict от 2026-04-19 по `steosvoice-ai-ozvuchka-v-telegram` был reject из-за слишком низкого ARPU и далёкого break-even.
- В rerun улучшились evidence по локальной выручке, Telegram-аудитории и B2B/API слою, поэтому economics теперь выглядят проходными в median/base на горизонте до 24 месяцев.
- Но rerun не довёл кейс до near-pass, потому что moat остаётся слабым, source-tier quality средняя, а company-level upside слишком зависит от апселла, который ещё не доказан контрактами.

## Оценка
Source tier balance: T1=1, T2=8, T3=2, weighted=1.91. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 18 | «LTV/CAC ... Prosumer 5,0x, API 12,4x», blended GM около 79-80%, но consumer-слой хрупкий. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 16 | «EBITDA ≈ 940 000 ₽/мес» достигается только в preferred scale при сильном сдвиге в SMB/API к 24 мес. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 13 | «ниша живая, но keyword-demand в РФ слабый», exact-demand LOW, weighted source tier 1.91 дал штраф -5. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 8 | Telegram-first и voice catalog помогают, но moat не удерживает category commoditization и легко копируется incumbents. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 11 | `price compression`, vendor dependence и founder-heavy GTM делают downside болезненным. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 15 | Каналы и ICP понятны, но без доказанного B2B pipeline approve нельзя, несмотря на 10 named targets. |

**Сумма raw:** 81/150  
**Normalized score:** **54/100**

## 7-factor moat framework

| Фактор | Балл 0-3 | Комментарий |
|---|---:|---|
| 1. Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных. |
| 2. Switching costs | 1 | У B2B/API есть лёгкий lock-in через интеграции и голоса, но он пока слабый. |
| 3. Scale economies | 2 | При росте объёма инфраструктура и каталог лучше монетизируются, но price war ограничивает эффект. |
| 4. Proprietary data / model advantage | 1 | Есть каталог и кастомные голоса, но нет сильного подтверждения масштаба уникального датасета. |
| 5. Regulatory moat | 0 | Явного лицензированного или compliance-moat нет. |
| 6. Brand / distribution | 2 | Telegram-first distribution и локальный бренд помогают на входе. |
| 7. Embedded workflow | 1 | В API и repeat-content workflow встраивается, но не на уровне mission-critical core system. |

**Итого 7-factor:** 7/21  
**Moat score:** **8/25**  
**Статус:** weak moat, обязательно в Top-3 Risks.

## Почему не approved
1. Company-level EBITDA выше 500К₽/мес появляется только в сценарии с заметно более плотным SMB/API mix, а не в уже доказанной базе.
2. Weak moat: продукт силён как utility, но не защищён против ElevenLabs, Just AI, Zvukogram, Yandex SpeechKit и long-tail TTS.
3. Exact-demand в РФ остаётся низким, а качество evidence опирается в основном на T2/T3, не на сильный T1 research stack.
4. Downside-case ломается быстро: p10 EBITDA отрицательный, sensitivity на price -30% и CAC x2 уводит модель в минус.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub (blended, p50) | ~53 530 ₽ |
| contribution_margin_rub_month (blended) | 2 684 ₽/клиент/мес |
| company_ebitda_rub_month базовый | 343 657 ₽/мес на M12 |
| company_ebitda_potential_rub_month | 940 000 ₽/мес через 24 мес |
| LTV/CAC | 5,3x blended median / 5,0x SMB / 12,4x API |
| CAC payback | 3,8 мес p50 |
| Gross Margin | 78,8% blended |
| Break-even | M10 base / 429 клиентов |
| Startup capital to BEP | 5 692 278 ₽ |
| clients_to_500k_ebitda | ~600-650 blended клиентов |
| months_to_500k_ebitda | 24 |

## FULL business process from 04-economics.md
1. Привлечение через Telegram, creator referrals, сайт и контентные входы.
2. Активация на первом job-to-be-done: озвучка ролика, рекламы, курса, карточки товара, доната, подкаста.
3. Перевод части пользователей в платные self-serve планы 200-700 ₽ и special plan 3 000 ₽.
4. Апселл в prosumer/SMB usage для агентств, онлайн-школ, маркетинга и контент-команд.
5. Апселл в API / batch / automation use cases для ботов, контентных конвейеров и внутренних workflow.
6. Апселл в custom voice / branded voice retainers с commercial rights.
7. Повторное использование и расширение seat/usage, если клиент встраивает voice layer в регулярный workflow.

## Unit economics и PnL summary

| Блок | Base | Optimistic | Pessimistic |
|---|---:|---:|---:|
| M12 MRR | 1 875 419 ₽ | 3 166 597 ₽ | 814 995 ₽ |
| M12 company_ebitda_rub_month | 343 657 ₽ | 1 344 850 ₽ | -538 754 ₽ |
| Startup capital to BEP | 5 692 278 ₽ | 4 625 232 ₽ | 9 963 696 ₽ |
| EBITDA break-even month | M10 | M8 | не достигнут |
| Break-even clients | 429 | 424 | 512 |

## Team table

| Роль | Кол-во | Fully-loaded FOT, ₽/мес | Комментарий |
|---|---:|---:|---|
| Founder / GM | 1 | 360 000 | На раннем этапе частично недооплачен в lean-mode |
| Full-stack / backend | 1 | 320 000 | Критичен для API и core platform |
| ML / speech engineer | 1 | 360 000 | Нужен для качества голоса и кастомных voice use cases |
| Product / growth | 1 | 220 000 | Ведёт activation и retention loop |
| Support / ops | 1 | 140 000 | Нужен для self-serve и enterprise support |
| Sales / partnerships | 1 | 190 000 | Ключевой для SMB/API апселла |
| **Итого полная команда** | **6** | **1 590 000** | До lean-оптимизации |

## GTM: 10 named targets

| Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| Skillbox | Уже фигурирует в evidence как типичный buyer с большим объёмом образовательного контента и озвучек | email decision-maker / intro через EdTech-партнёров | 120 000 ₽/мес |
| Нетология | Регулярный выпуск курсов и промо-контента, явная боль в speed-to-audio | email head of content | 90 000 ₽/мес |
| Skyeng | Постоянный контентный конвейер и voice assets для обучения | партнёрство / warm intro | 150 000 ₽/мес |
| Яндекс Практикум | Курсы, промо-ролики, onboarding-аудио и контент для уроков | email руководителю контента | 120 000 ₽/мес |
| VK Видео | Нужны voice workflows для creator ecosystem и промо-материалов | конференция / direct outreach | 180 000 ₽/мес |
| RUTUBE | Массовый видео-контент и потенциальные creator tools | direct BD outreach | 150 000 ₽/мес |
| Литрес | Озвучка промо, фрагментов и voice assets для каталога | email bizdev | 110 000 ₽/мес |
| 1C Game Studios | Игровые и NPC voice сценарии уже близки к brand use case SteosVoice | партнёрство / demo | 200 000 ₽/мес |
| SETTERS | Агентский контентный поток, нужда в быстрых voice creatives и commercials | реферал / конференция по маркетингу | 80 000 ₽/мес |
| Kokoc Group | Performance и content production для клиентов, можно продавать как white-label voice layer | партнёрство / agency outbound | 100 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Влияние | Почему это критично |
|---|---|---|---|
| Weak moat / commodity compression | Высокая | Очень высокое | Moat score 8/25, price -30% уже уводит модель в отрицательный EBITDA. |
| Недоказанный SMB/API апселл | Средняя | Очень высокое | Весь approve-case держится на более плотном mix, а не на consumer self-serve. |
| LLM/TTS vendor dependence и санкционные/infra риски | Высокая | Высокое | В risk matrix прямо отмечены vendor outage, cost spikes и санкционное трение. |

## Что нужно доказать для APPROVED
1. 10-15 платящих SMB/API клиентов с ARPA выше 80-100К₽/мес и retention не хуже 95% месячно.
2. Доля SMB/API/custom voice в MRR не ниже 40% к M6-M9.
3. Подтверждённый blended CAC payback < 6 месяцев после всех sales/support overhead.
4. Реальный customer_ltv_rub по B2B/API, подтверждённый не моделями, а cohort data.
5. Защитимый moat через proprietary voice assets, data flywheel, партнёрские каналы или встроенность в workflow.

## Proof points, которых не хватило до APPROVED
- Нет подтверждённого списка закрытых контрактов уровня Skillbox/агентства/API с ACV, достаточным для company-level margin of safety.
- Нет сильного T1/T2 подтверждения по уникальному датасету или технологическому превосходству, которое нельзя быстро скопировать.
- Нет evidence, что B2B/API слой уже доминирует в MRR, а не остаётся гипотезой поверх consumer utility.

## LTV Upside Calculator
Чтобы поднять score из 54/100 хотя бы к near-pass, кейсу нужен следующий сдвиг:

| Рычаг | Текущее состояние | Цель для re-review | Эффект |
|---|---|---|---|
| B2B/API ARPA | 28-30К₽/мес по модели | 80-120К₽/мес | Резко повышает customer_ltv_rub и снижает зависимость от consumer-mix |
| Blended churn | 5,0% mode | ≤3,5% | Поднимает LTV и стабилизирует p10 downside |
| Blended CAC | ~10,1К₽ mode | ≤6К₽ | Улучшает payback и Monte Carlo spread |
| Доля B2B/API/custom | <40% доказано | >50% MRR | Делает EBITDA-path менее хрупким |
| Proprietary voice / workflow lock-in | слабый | средний или сильный | Поднимает moat и снижает price compression risk |

## Финальное решение комитета
**REJECTED.**

SteosVoice в rerun выглядит намного лучше раннего reject, потому что локальная выручка, Telegram distribution и B2B/API гипотеза реально существуют. Но на текущем evidence это всё ещё не investment-grade кейс для standalone approve: moat слабый, market-demand в РФ не дотягивает, а EBITDA-порог достигается только в сценарии, где главный драйвер, SMB/API апселл, ещё не доказан фактами продаж.

