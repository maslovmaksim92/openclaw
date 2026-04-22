# 02-demand

## Demand Validation — RAAPID / autonomous medical coding, risk adjustment и revenue cycle automation в РФ

### Итог
**Решение на этапе P4: REJECTED.**

Причина: по обязательному demand API прямой спрос в РФ по core-category низкий, а Profit Gate не проходит ни в одном из реалистичных сценариев монетизации.

### 1) Demand signals
- Обязательный API по запросу `medical coding` вернул **LOW, score=15**: Habr = 2, HH = 3, Yandex Suggest = 100. Источник: `http://172.18.0.1:9001/multi-demand?keyword=medical%20coding` [T2, internal tool].
- Русскоязычный proxy-запрос `медицинский кодинг` тоже вернул **LOW, score=3**: Habr = 2, HH = 12, Yandex Suggest = 2. Источник: `http://172.18.0.1:9001/multi-demand?keyword=%D0%BC%D0%B5%D0%B4%D0%B8%D1%86%D0%B8%D0%BD%D1%81%D0%BA%D0%B8%D0%B9%20%D0%BA%D0%BE%D0%B4%D0%B8%D0%BD%D0%B3` [T2, internal tool].
- Запрос `risk adjustment` в РФ также дал **LOW, score=0**. Источник: `http://172.18.0.1:9001/multi-demand?keyword=risk%20adjustment` [T2, internal tool].
- Это согласуется со структурой российского рынка: в РФ есть крупный рынок частной медицины, но американский pain around coding / claims / risk-adjustment почти не переносится 1:1 из-за другой модели оплаты, более слабой роли CPT-style billing и меньшей зрелости отдельной категории revenue cycle SaaS. Инференс на базе low-demand сигналов и структуры рынка [T1/T2 inference].

### 2) Конкуренты с ценами
Курс для перевода: **1 USD = 74,5897 ₽**. Источник: ЦБ РФ на 22.04.2026 [T1], https://www.cbr.ru/currency_base/daily/

| Конкурент | Цена | Цена в ₽ | Комментарий |
|---|---:|---:|---|
| athenaOne Medical Billing | 4-7% collections | зависит от выручки клиники | Классический RCM/billing benchmark, публично quoted pricing через Tebra [T2]. Источник: https://www.tebra.com/theintake/practice-growth/healthcare-billing-software-pricing-guide |
| AdvancedMD Medical Billing | 4-9% collections | зависит от выручки клиники | Один из прямых substitutes по billing/coding workflow [T2]. Источник: https://www.tebra.com/theintake/practice-growth/healthcare-billing-software-pricing-guide |
| DrChrono Revenue Cycle Management | 3-8% collections | зависит от выручки клиники | Ещё один публичный pricing anchor по RCM [T2]. Источник: https://www.tebra.com/theintake/practice-growth/healthcare-billing-software-pricing-guide |
| Tebra Billing Software | от $150/мес | от ~11 188 ₽/мес | Низкий порог для software-only billing stack [T2]. Источник: https://www.tebra.com/theintake/practice-growth/healthcare-billing-software-pricing-guide |

Вывод по конкурентам: в США category pricing держится либо на процентах от сборов, либо на фиксированном billing-SaaS чеке. Для РФ такой pricing anchor плохо переносится, потому что локальный billing stack и unit economics клиник слабее [T2 inference].

### 3) Проверка Telegram / ботов и сервисов в РФ
- В РФ Telegram используется в медицине в основном для записи, FAQ, triage и patient support, а не для autonomous medical coding [T2].
- **1Meda** предлагает Telegram-бот для клиник под запись пациентов и обработку обращений; публичного прайса на лендинге нет, то есть это не transparent software category, а скорее кастомный service-led workflow [T2]. Источник: https://1meda.ru/bot.html
- **GIDMedical** продаёт Telegram-бот для ответов на медвопросы по **1 950 ₽/мес** или **1 250 ₽ за 2 недели**; это B2C/patient-support сервис, не coding/RCM [T2]. Источник: https://www.gidmedical.ru/
- **BotCreators / similar clinic-bot integrators** на рынке РФ продают разработку Telegram-ботов для клиник как агентскую услугу, а не productized coding stack; typical market framing через разовую разработку и кастомизацию подтверждает незрелость отдельной product-category [T2/T3].
- Публично заметных Telegram-ботов именно для medical coding / risk adjustment / autonomous claims QA в РФ не найдено. Вывод: Telegram как канал релевантен для patient acquisition и support, но **не подтверждает локальный спрос на RAAPID-like product** [T2 inference].

### 4) WTP, willingness to pay
- На развитом рынке WTP доказан: athenaOne, AdvancedMD, DrChrono и Tebra публично продают billing/RCM и берут либо проценты от collections, либо фиксированный monthly fee [T2]. Это подтверждает, что provider-side buyers готовы платить за ускорение cash collection и coding accuracy.
- В РФ публичное доказательство WTP именно за autonomous medical coding слабое. Нашлись платежи за adjacent-медботы, запись, patient support и за general clinic automation, но не за standalone coding/risk-adjustment SKU [T2].
- Следовательно, **WTP в РФ по core-category остаётся гипотезой**, а не подтверждённым инвестиционным фактом. Есть willingness to pay за adjacent automation, но не за тот wedge, с которым RAAPID продаётся в США [T2/T3, low confidence].

### 5) Market sizing
#### Допущения
- Курс: **74,5897 ₽ / USD** [T1].
- Объём рынка платных медицинских услуг в РФ в 2025 году: **1,87 трлн ₽** [T2, со ссылкой на Росстат]. Источник: https://eqiva.ru/articles/analitika/rynok-platnykh-meditsinskikh-uslug-v-rossii-itogi-2025-goda/
- Число частных медицинских организаций в РФ: **66 031** [T2]. Источник: https://marketing.rbc.ru/articles/16251/
- В крупнейших городах оборот частных клиник в 2024 году оценивался в **822 млрд ₽** [T2]. Источник: https://medvestnik.ru/content/news/Rost-oborota-chastnyh-klinik-v-Rossii-v-2024-godu-ocenili-v-16.html
- Для bottom-up беру стартовый ICP: крупные частные сети, лаборатории, диагностические группы, клиники с высоким объёмом ДМС/платных услуг. Средний реалистичный ARR для локального coding-QA / audit / workflow слоя принимаю **1,2 млн ₽/год** на организацию, то есть ~100k ₽ MRR [T2/T3 inference].

#### Top-down
- **TAM (мир)**: глобальный рынок medical coding market в 2025 году оценивается в **$43,85 млрд** [T2]. В рублях это **~3,27 трлн ₽** по курсу ЦБ.
- **TAM (РФ)**: беру рынок платных медуслуг РФ **1,87 трлн ₽** [T2] и адресуемую долю **1,5%** на billing/coding/revenue-integrity software + managed QA слой. Получаем **28,1 млрд ₽** [T2 inference].
- **SAM (РФ)**: для реального входа оставляю только частную медицину и крупные коммерческие сегменты с достаточной сложностью документооборота, то есть **25% TAM_RF = 7,0 млрд ₽** [T2 inference].
- **SOM Y1**: 2% от SAM = **140 млн ₽** [inference].
- **SOM Y3**: 6% от SAM = **421 млн ₽** [inference].

#### Bottom-up
10 реальных buyers для первого ICP в РФ [T2]: Медси, Мать и дитя, EMC, СМ-Клиника, Медскан, АВА-ПЕТЕР/Скандинавия, Поликлиника.ру, Семейный доктор, Клиника Фомина, Инвитро. Источники: рейтинг крупнейших медицинских компаний Forbes 2025 [T2], отраслевые публикации о частных клиниках [T2].

Bottom-up расчёт:
- Total buyers = **66 031** частных медорганизаций [T2].
- % with need = **3%**. Это только сети и организации, где есть заметная доля платных услуг, сложный документооборот и достаточный объём ручного QA/coding pain. Поддержка: низкий прямой demand, но ненулевой adjacent pain и наличие крупного частного сегмента [T2 inference].
- ARR avg = **1,2 млн ₽/год**.
- **SAM_bottom-up** = 66 031 × 3% × 1,2 млн ₽ = **2,38 млрд ₽**.
- **SOM_bottom-up Y1** = 1% от SAM_bottom-up = **23,8 млн ₽**.
- **SOM_bottom-up Y3** = 4% от SAM_bottom-up = **95,1 млн ₽**.

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 3,27 трлн ₽ [T2+T1] | — | — | top-down |
| TAM (РФ) | 28,1 млрд ₽ [T2 inference] | 79,2 млрд ₽ if 66 031 × 100% × 1,2 млн ₽ [T2 inference] | diff >3x; full private-clinic base завышает реальную addressability, поэтому TAM_RF ограничиваю top-down | **lower** |
| SAM (РФ) | 7,0 млрд ₽ [T2 inference] | 2,38 млрд ₽ [T2 inference] | diff 2,9x, допустимо после ужесточения ICP | **lower** |
| SOM Y1 | 140 млн ₽ | 23,8 млн ₽ | diff 5,9x, top-down слишком оптимистичен для slow enterprise sales | **используем 23,8 млн ₽** |
| SOM Y3 | 421 млн ₽ | 95,1 млн ₽ | diff 4,4x, top-down агрессивен | **используем 95,1 млн ₽** |

Итог по sizing: даже после reconciliation в РФ виден только **узкий niche-SAM**, а не широкий market. Это недостаточно для уверенного тезиса geo-expand без сильного локального wedge.

### 6) Profit Gate (цель EBITDA компании >= 500k ₽/мес)
Проверяю все реалистичные сценарии.

**Сценарий A. Self-serve / software-only для небольших клиник**
- Цена: **100k ₽/мес** на клинику.
- При gross margin 80% и минимальном локальном opex **1,5 млн ₽/мес** нужна выручка **~2,5 млн ₽/мес**, то есть **25 клиник**.
- Для категории с low-demand, без явного РФ category pull и с длинным внедрением даже 25 платящих клиник выглядят чрезмерно оптимистично. **FAIL**.

**Сценарий B. Managed audit + coding QA service**
- Цена: **250k ₽/мес** на крупную сеть/лабораторную группу.
- При gross margin 60% и opex **2,0 млн ₽/мес** нужен MRR **~4,17 млн ₽**, то есть **17 аккаунтов**.
- Такой объём крупных платящих аккаунтов для узкого и плохо понятного buyer pain в РФ выглядит недостижимым в разумный срок. **FAIL**.

**Сценарий C. Enterprise on-prem / hybrid revenue-integrity platform**
- Цена: **600k ₽/мес** на enterprise-сеть.
- При gross margin 65% и opex **2,5 млн ₽/мес** нужен MRR **~4,62 млн ₽**, то есть минимум **8 enterprise-контрактов**.
- Но именно enterprise-модель требует самых длинных циклов закупки, интеграций с МИС/ERP и локальной клинической адаптации. Для рынка с LOW direct demand это слишком тяжёлый go-to-market. **FAIL**.

**Вывод Profit Gate:** во всех сценариях достижение **EBITDA >= 500k ₽/мес** требует слишком большого числа клиентов для категории, где локальный demand pull почти не подтверждён. **Profit Gate FAIL.**

### 7) Финальный вывод
- **DEMAND = LOW** по обязательным core и proxy запросам.
- **Profit Gate = FAIL** по всем основным моделям монетизации.
- По правилу early reject кейс должен быть **отклонён уже на этапе demand validation**.

### Источники
- [T1] ЦБ РФ daily rates: https://www.cbr.ru/currency_base/daily/
- [T2] Demand API: internal multi-demand URLs above
- [T2] Tebra billing software pricing guide: https://www.tebra.com/theintake/practice-growth/healthcare-billing-software-pricing-guide
- [T2] Рынок платных медуслуг РФ 2025: https://eqiva.ru/articles/analitika/rynok-platnykh-meditsinskikh-uslug-v-rossii-itogi-2025-goda/
- [T2] Частные медорганизации РФ: https://marketing.rbc.ru/articles/16251/
- [T2] Оборот частных клиник: https://medvestnik.ru/content/news/Rost-oborota-chastnyh-klinik-v-Rossii-v-2024-godu-ocenili-v-16.html
- [T2] Forbes private medical companies ranking 2025: https://www.forbes.ru/rating/551134-lidery-rejtinga-krupnejsih-medicinskih-kompanij-2025/
- [T2] 1Meda Telegram bot: https://1meda.ru/bot.html
- [T2] GIDMedical pricing: https://www.gidmedical.ru/
- [T2] Global medical coding market: https://www.precedenceresearch.com/medical-coding-market

Sources: T1=1, T2=9, T3=0. Primary evidence basis: T2.
