---
stage: demand-validation
case: corgi-startup-insurance-geo-expand-v2
date: 2026-04-21
analyst: branch-models-lead
sector: FINTECH
verdict: FAIL
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
Corgi как AI-native full-stack страховая платформа для стартапов и tech-компаний: instant quote, modular coverage, D&O, Tech E&O, Cyber и смежные полисы под стадии Pre-Seed, Series A и Growth.

## Итог
**Статус: FAIL.**

На 21 апреля 2026 года кейс выглядит интересным как продуктовая digitization-story для insurtech, но не проходит demand gate Program 2 как high-LTV GEO-EXPAND opportunity.

Причины:
1. Corgi прямо продаёт пакетное страхование стартапов, но публичный ценовой якорь на сайте остаётся слишком низким для нашего порога: **$2k-5k в год** для pre-seed и **$5k-15k в год** для Series A, то есть это примерно **15-112 тыс. ₽ в месяц** при грубом FX-пересчёте, а не `>500 тыс. ₽/мес` на аккаунт. [T1]
2. Даже если добавлять D&O, Cyber, Tech E&O и другие модули, модель Corgi на сайте выглядит как быстрый self-serve / low-friction insurance motion, а не как тяжёлый managed high-ticket operating layer. [T1][T2]
3. В локальном контуре РФ adjacent budget lines существуют, это подтверждают как минимум официальные правила Ингосстраха по страхованию ответственности директоров и публичное внедрение ИИ в тарифообразование у СберСтрахования жизни, но эти сигналы говорят скорее о наличии корпоративного страхового рынка вообще, а не о готовности покупать узкий startup-insurance stack с чеком уровня Program 2. [T4][T5]
4. Exact-demand сигналы по `startup insurance` и `страхование стартапов` слабые, а по `D&O insurance startup`, `cyber insurance startup` и `D&O страхование стартап` фактически отсутствуют. [T3]

Итоговый вывод: category proof есть, но он ведёт в сторону низкого SMB/startup ARPU и тяжёлой локальной регуляторики. Для Program 2 это early reject уже на demand-этапе.

## 1. Сигналы спроса

### Exact-demand check
Источник: internal multi-demand API.

- `startup insurance` -> demand score **7**, без сильного публичного хвоста по job/search signals. [T3]
- `страхование стартапов` -> demand score **7**, также без сильных подтверждающих хвостов. [T3]
- `D&O insurance startup` -> demand score **0**. [T3]
- `cyber insurance startup` -> demand score **0**. [T3]
- `D&O страхование стартап` -> demand score **0**. [T3]

### Интерпретация
- В отличие от enterprise cyber, fintech infra или compliance-ops, здесь не видно сильного exact-category спроса даже на англоязычных формулировках.
- В РФ потребность, если и существует, скорее растворена внутри более широких категорий: страхование ответственности директоров, киберриски, профессиональная ответственность, страхование для VC-backed бизнеса.
- Это плохой сигнал именно для GEO-EXPAND кейса, потому что для запуска пришлось бы одновременно делать category creation, лицензирование, carrier-партнёрства и объяснять новый wedge рынку.

## 2. Category proof и what is actually being bought
1. Corgi на официальном сайте называет себя **first full-stack AI insurance company** и продаёт instant quotes plus modular coverage для стартапов. [T2]
2. На продуктовой странице Corgi разбивает предложение по стадиям компании, а ключевыми покрытиями называет **D&O, Tech E&O, Cyber, EPLI, Fiduciary, Media** и другие модули. [T1]
3. Сам Corgi объясняет, что Series A пакет нужен стартапам, которые поднимают венчурный капитал, подписывают enterprise contracts или проходят SOC 2. Это хороший proof того, что pain реально существует. [T1]
4. Но одновременно Corgi раскрывает price anchors: pre-seed обычно **$2k-5k в год**, Series A обычно **$5k-15k в год**. Это сразу задаёт категорию как низко- или умеренно-чековую относительно нашего investment screen. [T1]

### Вывод
Покупается не «AI underwriting platform» как дорогой enterprise workflow, а набор относительно стандартных страховых полисов, просто лучше упакованный и быстрее выдаваемый.

## 3. Локальный контур РФ
1. В РФ корпоративные insurance budget lines реально существуют. Ингосстрах публикует официальные правила страхования ответственности директоров и руководителей, то есть D&O как продукт в локальном контуре не экзотика. [T4]
2. СберСтрахование жизни публично сообщало о внедрении ИИ в тарифообразование ипотечного страхования жизни и отдельно называло ИИ одним из главных трендов отрасли. Это подтверждает, что российский insurance market уже движется в сторону automation. [T5]

### Но это не спасает кейс
- Эти факты подтверждают зрелость страхового рынка и цифровизацию, но не показывают, что локальные стартапы готовы массово покупать специализированый startup-insurance stack по high-ticket модели.
- Скорее наоборот: если локальный рынок уже обслуживается крупными страховщиками и брокерами, то для нового GEO-EXPAND игрока барьеры выше, а дифференциация сложнее.
- Дополнительно накладываются лицензирование, compliance, carrier-capacity, перестрахование и юридическая адаптация. Для low-ticket motion это особенно плохо.

## 4. WTP и ценовой потолок

### Публичные якоря willingness to pay
- Pre-seed: **$2k-5k в год**. [T1]
- Series A: **$5k-15k в год**. [T1]
- Corgi также обещает quote за **under 10 minutes** и same-day binding, то есть value prop строится вокруг скорости и удобства, а не вокруг крупного enterprise transformation spend. [T1][T2]

### Перевод в Program 2 economics
Даже если грубо принять диапазон **90 ₽ за $1** как рабочую оценку для sanity-check:
- **$2k/год ≈ 180 тыс. ₽/год ≈ 15 тыс. ₽/мес**
- **$15k/год ≈ 1,35 млн ₽/год ≈ 112,5 тыс. ₽/мес**

Это на порядок ниже целевого уровня `>500 тыс. ₽/мес` на клиента.

## 5. Profit Gate

### Сценарий A: self-serve startup insurance
- Средний чек: **60 тыс. ₽/мес**
- Валовая маржа: **35%** как грубый inference для страхового / distribution motion
- Валовая прибыль на клиента: **21 тыс. ₽/мес**
- Для EBITDA **500 тыс. ₽/мес** понадобятся десятки аккаунтов даже без тяжёлых fixed costs
- **Вердикт: FAIL**

### Сценарий B: growth-stage / custom package
- Средний чек: **110 тыс. ₽/мес** по верхней публичной вилке Corgi [T1]
- Даже при валовой марже **40%** валовая прибыль на клиента около **44 тыс. ₽/мес**
- Для целевого EBITDA всё ещё нужен слишком большой объём аккаунтов
- **Вердикт: FAIL**

### Сценарий C: гипотетический premium managed broker layer
- Можно вообразить более дорогой packaged risk-management motion для финтеха, AI и healthtech
- Но это уже заметное отклонение от того, что Corgi публично продаёт сегодня [inference]
- Подтверждённых ценовых якорей на `>500 тыс. ₽/мес` нет
- **Вердикт: FAIL**

## 6. Основные риски
- Низкий ticket size относительно порога программы. [T1]
- Слабый exact-demand. [T3]
- Очень тяжёлая локализация: лицензии, carrier partnerships, compliance, wordings, claims operations. [T4][inference]
- Риск, что вся ценность кейса сводится к интерфейсу и automation над уже commoditized insurance products. [T1][T2]

## 7. Решение для pipeline
**Отклонить кейс на этапе demand validation.**

Почему:
1. категория реальна, но чек слишком низкий;
2. локальный demand слабый и не компенсирует regulatory burden;
3. adjacent proof в РФ подтверждает существование страхового рынка, но не high-LTV GEO-EXPAND окно;
4. модель больше похожа на productized SMB insurance, чем на premium operator thesis.

## Market Pulse
Market Pulse 21.04.2026: нейтрально-негативный.

Интерес к цифровизации страхования и ИИ в insurance есть, но именно startup-insurance wedge выглядит слишком мелким по выручке на аккаунт и слишком тяжёлым по запуску для критериев программы.

## Источники
- [T1] Corgi Startup Insurance, accessed 2026-04-21: https://www.corgi.insure/startup-insurance
- [T2] Corgi homepage / about, accessed 2026-04-21: https://www.corgi.insure/ ; https://www.corgi.insure/about
- [T3] Multi-demand API: http://172.18.0.1:9001/multi-demand?keyword=startup%20insurance ; http://172.18.0.1:9001/multi-demand?keyword=%D1%81%D1%82%D1%80%D0%B0%D1%85%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20%D1%81%D1%82%D0%B0%D1%80%D1%82%D0%B0%D0%BF%D0%BE%D0%B2 ; http://172.18.0.1:9001/multi-demand?keyword=D%26O%20insurance%20startup ; http://172.18.0.1:9001/multi-demand?keyword=cyber%20insurance%20startup ; http://172.18.0.1:9001/multi-demand?keyword=D%26O%20%D1%81%D1%82%D1%80%D0%B0%D1%85%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20%D1%81%D1%82%D0%B0%D1%80%D1%82%D0%B0%D0%BF
- [T4] Ингосстрах, правила страхования ответственности директоров, accessed 2026-04-21: https://cdn.ingos.ru/docs/Directors_Liability_Insurance_Rules.pdf
- [T5] СберСтрахование жизни, 2024-06-18 и 2024-04-26: https://sberbank-insurance.ru/news/view?slug=18_06_24 ; https://sberbank-insurance.ru/news/26_04_24

Sources: T1=1, T2=2, T3=5, T4=1, T5=2. Primary evidence basis: T1/T3/T4.

> Market Pulse 22.04.2026: наблюдается рост интереса по текущим веб-сигналам.
