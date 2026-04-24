---
stage: demand-validation
case: superdial-insurer-calls-geo-expand-v2
date: 2026-04-24
analyst: branch-models-lead
sector: HEALTHCARE
verdict: REJECTED
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
SuperDial: automation layer для звонков клиник и billing/RCM-команд страховщикам, verification, denial follow-up и payer-call workflows.

## Итог
**Решение на этапе demand validation: REJECTED.**

- В РФ exact-demand на US-style payer-call automation выглядит **LOW**. Обязательный demand endpoint по запросам `автоматизация звонков в страховую`, `проверка страхового покрытия клиника`, `согласование со страховой клиника` возвращает LOW; только широкий adjacent keyword `дмс клиника` даёт MEDIUM, но это рынок ДМС в целом, а не отдельная категория insurer-call automation. [T2]
- Underlying spend в ДМС и координации действительно существует: Банк России пишет, что по итогам 9 месяцев 2025 года работодатели застраховали почти **20 млн** сотрудников, а премии по ДМС от работодателей выросли до **191,3 млрд ₽**. Это подтверждает наличие большого денежного контура, но не доказывает спрос именно на продукт SuperDial. [T1]
- Реальные публичные substitute-решения с ценами существуют, но они в основном продают **generic AI front desk / phone automation**, а не insurer-call revenue-cycle automation. Публичные ценовые точки находятся в диапазоне от **$99/мес** до **$399/мес** и **$0,09/мин**, то есть buyer expectation по автоматизации звонков скорее низко- и среднечековая, а не high-ACV category. [T2]
- В РФ Telegram-боты и сервисы вокруг клиник уже есть, но они закрывают запись, маршрутизацию и patient communication, а не payer-call wedge. Это дополнительный признак, что локальный рынок monetizes patient access / clinic ops, а не US-style insurer RCM automation. [T2][T3]
- **Profit Gate в текущем позиционировании не проходит.** Для standalone бизнеса нужно либо много низкочековых логотипов, либо few-account enterprise motion, на который в РФ нет достаточного прямого спроса и ценовых якорей. [T1][T2][inference]

## 1) Demand signals

### Demand API
- `автоматизация звонков в страховую` → **LOW**, `demand_score=3`, `hh_ru=15`, `yandex_suggest=2`. [T2]
- `проверка страхового покрытия клиника` → **LOW**, `demand_score=0`, `hh_ru=1`, `yandex_suggest=2`. [T2]
- `согласование со страховой клиника` → **LOW**, `demand_score=3`, `hh_ru=49`, `yandex_suggest=2`. [T2]
- `дмс клиника` → **MEDIUM**, `demand_score=31`, `hh_ru=7903`, `yandex_suggest=100`. [T2]
- `denial management healthcare` → **LOW**, `demand_score=0`. [T2]
- `prior authorization automation` → **LOW**, `demand_score=0`. [T2]

### Интерпретация
- В РФ есть большой adjacent market вокруг ДМС, клиник и медицинской координации, но **нет выраженного local category pull** на denial-management / prior-auth / payer-call automation как отдельный software budget line. [T1][T2][inference]
- Это критично, потому что SuperDial продаёт не просто телефонию, а очень конкретный workflow: звонки страховщикам ради verification, authorization и status follow-up. Такой workflow в РФ заметно слабее оформлен как самостоятельная vendor category, чем в США. [T2][T3][inference]

## 2) Реальные конкуренты с ценами

Ниже, не идеальные копии SuperDial, а реальные substitute/adjacent competitors в call automation, через которых видно buyer price anchor.

| Конкурент | Что продаёт | Публичная цена | Что это значит |
|---|---|---:|---|
| My AI Front Desk | AI phone receptionist / front desk automation | **от $99/мес**, Growth **$149/мес**, overage **$0.25/мин** [T2] | Малый и средний buyer привык к низкому входному чеку за AI call automation |
| Loman AI | AI phone agent | Starter **от $199/мес**, Premium **от $399/мес** [T2] | Даже у более развитого voice automation pricing остаётся относительно низким |
| AutoCalls | AI voice agent / white-label voice platform | Starter **$27/мес**, Growth **$103/мес**, Agency **$199/мес**, White Label **$355/мес**, usage **от $0.09/мин** [T2] | Рынок commoditizes voice layer и давит на ARPU |

### Read-through по конкурентам
- Эти цены **не подтверждают** high-ACV рынок для insurer-call automation в РФ. Наоборот, они показывают, что нижняя часть рынка уже воспринимает voice AI как дешёвый automation layer. [T2][inference]
- Чтобы выйти на fundable economics, SuperDial в РФ пришлось бы продавать не «AI звонки», а тяжёлый enterprise workflow platform с интеграцией в клинику/страховщика. Но публичных локальных сигналов спроса на такой wedge я не нашёл. [T2][T3][inference]

## 3) Telegram bots / services в РФ

Найденные локальные сигналы:
- **Medesk** продвигает Telegram-бот для клиник как канал записи и коммуникации с пациентами. Это подтверждает, что Telegram в РФ уже monetized в clinic ops, но не в insurer-call workflows. [T2]
- В блоге Medesk описан сервис **Medidea**: бот помогает записаться в клинику, вызывает врача на дом, подбирает врача и может направлять запрос на ДМС; цена в публикации указана **от 6 900 ₽/мес**. [T2]
- Demand API по исследуемым insurer-call ключам не показывает сильных TG signals; `telegram subscribers=0` по проверенным ключам. [T2]

**Вывод:** Telegram в РФ применим как patient communication / lead capture / запись, но не как убедительное подтверждение рынка insurer-call automation. Для кейса это скорее **negative-to-neutral signal**. [T2][inference]

## 4) WTP, proof of willingness to pay

### Что реально подтверждено
1. **ДМС как бюджетный контур существует.** Банк России фиксирует почти **20 млн** застрахованных сотрудников и **191,3 млрд ₽** премий работодателей по ДМС за 9 месяцев 2025 года. [T1]
2. **Клиники уже покупают цифровые каналы и ботов.** Есть публичные Telegram/бот-сервисы для клиник с рублёвым ценником, например Medidea от **6 900 ₽/мес**. [T2]
3. **Voice automation globally monetized**, но по относительно низким ценам: от **$99-399/мес** и/или usage-based model. [T2]

### Что НЕ подтверждено
- Не найдено доказательств, что в РФ buyer готов платить premium-чек именно за **payer-call / denial-management / prior-authorization automation** как отдельный продукт. [T2][T3]
- Не найдено локальных публичных прайсов или кейсов, где российская клиника или страховщик уже покупает insurer-call automation в масштабе, достаточном для enterprise software economics. [T2][T3]

### Вывод по WTP
**WTP = LOW-MEDIUM и только для adjacent clinic ops automation.** Для точного кейса SuperDial willingness to pay остаётся недостаточно доказанной. [T1][T2][T3][inference]

## 5) Market sizing

### Методика
Считаю двумя путями и намеренно беру консервативные цифры. Здесь важно не перепутать большой рынок ДМС с маленьким software-layer для insurer-call automation.

### 10 реальных buyers для bottom-up / GTM targets
1. Медси [T2]
2. Мать и дитя [T2]
3. EMC [T2]
4. СМ-Клиника [T2]
5. Семейный доктор [T2]
6. Будь Здоров [T2]
7. MedSwiss [T2]
8. Скандинавия / АВА-ПЕТЕР [T2]
9. Ингосстрах ДМС [T2]
10. СОГАЗ ДМС [T2]

Это реальные потенциальные покупатели/партнёры для смежного workflow, но не доказанные текущие клиенты или подтверждённые deployable accounts. [T2][inference]

### Top-down
- База: корпоративный ДМС, **191,3 млрд ₽** премий за 9 месяцев 2025 года. [T1]
- Для software-layer, который автоматизирует именно согласования/verification/call workflows между клиникой и страховщиком, беру addressable share **0,3-0,8%** от премий. Это уже агрессивно для узкого admin layer. [T1][T2][inference]
- Тогда **TAM (РФ)** = **574 млн - 1,53 млрд ₽**.
- Для консервативной модели беру нижнюю часть и считаю **SAM** как 40% от TAM, доступные крупные private clinics + DMS-heavy insurers.
- **SAM top-down** = **230 млн ₽**.
- **SOM Y1 top-down** = 2% от SAM = **4,6 млн ₽**.
- **SOM Y3 top-down** = 8% от SAM = **18,4 млн ₽**.

### Bottom-up
- Total buyers: **~400** потенциальных аккаунтов, где действительно есть заметный объём ДМС-координации, звонков, pre-approval и ручного статуса. Это допущение по крупным/средним private clinics, hospital groups и DMS-insurer operations. [T2][T3][inference]
- % with need: **25%**. Это поддерживается тем, что adjacent keyword `дмс клиника` даёт MEDIUM и очень высокий hh proxy, но exact workflow-keywords остаются LOW. [T2]
- ARR avg: **1,8 млн ₽/год** на аккаунт, то есть примерно **150 тыс. ₽/мес** blended contract. Это уже выше публичных generic voice-bot прайсов и требует интеграции, но ещё ниже настоящего enterprise platform spend. [T2][T3][inference]
- **SAM_bottom_up** = 400 × 25% × 1,8 млн ₽ = **180 млн ₽**.
- **SOM_bottom_up Y1** = 10 клиентов × 1,8 млн ₽ = **18 млн ₽**.
- **SOM_bottom_up Y3** = 20 клиентов × 1,8 млн ₽ = **36 млн ₽**.

### Обязательная таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | — | — | Для этого кейса считаю только РФ, потому что оцениваем GEO-expand wedge | — |
| TAM (РФ) | 574 млн ₽ [T1][inference] | 720 млн ₽ = 400 buyers × 100% need × 1,8 млн ₽ [T2][T3][inference] | diff ~1,25x, допустимо для узкой категории | lower |
| SAM (РФ) | 230 млн ₽ [T1][T2][inference] | 180 млн ₽ [T2][T3][inference] | diff ~1,28x, допустимо | lower |
| SOM Y1 | 4,6 млн ₽ | 18 млн ₽ | top-down заметно строже; беру lower bound из-за низкого exact-demand | **используем 4,6 млн ₽** |
| SOM Y3 | 18,4 млн ₽ | 36 млн ₽ | разброс объясняется optimistic capture в bottom-up | **используем 18,4 млн ₽** |

### Sanity checks
- Расхождение top-down и bottom-up по SAM < 3x, модель допустима.
- SOM Y1 < 10% SAM, overclaiming нет.
- Но даже консервативный SOM Y1 очень мал для software-first venture wedge. [T1][T2][inference]

## 6) Profit Gate: проверка всех сценариев

### Scenario A: дешёвый self-serve voice bot для клиник
- Ценовой коридор по рынку близок к **$99-399/мес** или низким рублёвым подпискам. [T2]
- При таком ARPU для EBITDA **500 тыс. ₽/мес** нужны десятки и скорее сотни установок, плюс локальная поддержка и интеграции.
- **Вердикт: FAIL.** [T2][inference]

### Scenario B: mid-market clinic DMS coordination copilot
- Допущение: **80-150 тыс. ₽/мес** на аккаунт. [T2][T3][inference]
- Чтобы выйти на EBITDA 500 тыс. ₽/мес, нужно примерно **20-30** активных клиентов при заметной support/integration нагрузке.
- При текущем LOW exact-demand и длинном sales-assisted motion это выглядит ненадёжно.
- **Вердикт: FAIL.** [T2][inference]

### Scenario C: enterprise platform для крупных клиник и страховщиков
- Здесь возможен чек **300-500 тыс. ₽/мес**, но для него нет подтверждённого локального category pull, публичных референсов и strong pricing evidence. [T2][T3]
- Это уже не SuperDial-as-is, а broader workflow platform / systems-integration motion.
- **Вердикт: CONDITIONAL FAIL.** Как теоретический pivot, не как подтверждённый текущий кейс. [T2][T3][inference]

## 7) Почему кейс уходит в early reject
Условие программы выполнено:
- **DEMAND = LOW** для точного кейса insurer/payer call automation. [T2]
- **Profit Gate FAIL** в текущем позиционировании: ни self-serve, ни mid-market, ни правдоподобный enterprise сценарий не дают достаточно надёжного пути к **EBITDA ≥ 500 тыс. ₽/мес** в РФ без существенного product pivot. [T2][inference]

Следовательно, кейс должен быть **REJECTED** уже на demand-stage и перемещён в `pipeline/rejected/`. [inference]

## 8) Что могло бы изменить решение
1. Публичные локальные кейсы клиник/страховщиков РФ именно по automated insurer-call / pre-approval / status follow-up. [T2]
2. Подтверждённые контракты хотя бы **300-500 тыс. ₽/мес** на 3-5 аккаунтах в РФ. [T2]
3. Доказательство, что продукт можно продать как enterprise DMS workflow system, а не как commoditized voice-bot layer. [T2][T3]

## Источники
- [T1] Банк России, 01.12.2025: «Премии по ДМС от работодателей выросли до 191,3 млрд рублей», почти 20 млн застрахованных сотрудников: https://www.cbr.ru/press/event/?id=23528
- [T2] Demand API, просмотрено 24.04.2026:
  - http://172.18.0.1:9001/multi-demand?keyword=%D0%B0%D0%B2%D1%82%D0%BE%D0%BC%D0%B0%D1%82%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F%20%D0%B7%D0%B2%D0%BE%D0%BD%D0%BA%D0%BE%D0%B2%20%D0%B2%20%D1%81%D1%82%D1%80%D0%B0%D1%85%D0%BE%D0%B2%D1%83%D1%8E
  - http://172.18.0.1:9001/multi-demand?keyword=%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20%D1%81%D1%82%D1%80%D0%B0%D1%85%D0%BE%D0%B2%D0%BE%D0%B3%D0%BE%20%D0%BF%D0%BE%D0%BA%D1%80%D1%8B%D1%82%D0%B8%D1%8F%20%D0%BA%D0%BB%D0%B8%D0%BD%D0%B8%D0%BA%D0%B0
  - http://172.18.0.1:9001/multi-demand?keyword=%D1%81%D0%BE%D0%B3%D0%BB%D0%B0%D1%81%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20%D1%81%D0%BE%20%D1%81%D1%82%D1%80%D0%B0%D1%85%D0%BE%D0%B2%D0%BE%D0%B9%20%D0%BA%D0%BB%D0%B8%D0%BD%D0%B8%D0%BA%D0%B0
  - http://172.18.0.1:9001/multi-demand?keyword=%D0%B4%D0%BC%D1%81%20%D0%BA%D0%BB%D0%B8%D0%BD%D0%B8%D0%BA%D0%B0
  - https://www.myaifrontdesk.com/pricing
  - https://loman.ai/pricing
  - https://autocalls.ai/pricing
  - https://www.medesk.net/ru/blog/telegram-bot-dlya-kliniki/
  - https://www.medesk.net/ru/blog/medidea-bot-dlja-kliniki/
- [T3] Supporting / low-confidence context:
  - https://www.medesk.net/ru/blog/insurance-programs-in-a-clinic/
  - search evidence on local clinic automation packaging and Telegram-first workflows

## Market Pulse
Market Pulse 24.04.2026: слабый спрос на точный кейс, сильнее только adjacent контур ДМС и clinic ops.

Sources: T1=1, T2=8, T3=2. Primary evidence basis: T2.