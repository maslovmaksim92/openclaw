# 02-demand

## Demand validation summary
- **Продукт**: EvenUp-подобная AI-платформа для plaintiff-side personal injury, demand letters и расчета ущерба по массовым делам. Для РФ это узкий wedge, потому что местный рынок менее contingency-driven, а personal-injury как отдельная software category почти не сформирована. [T1/T2, inference]
- **Итог по спросу в РФ**: **LOW**. Mandatory endpoint по максимально близким pain-keywords вернул LOW: `юридический ИИ для исков` → **3/100**, `составление исков онлайн` → **3/100**, `автоматизация юридических документов` → **15/100**. Это означает, что category pull для plaintiff-claims AI в РФ слабый, а поисковый и контентный спрос находится в ранней стадии. [T2: http://172.18.0.1:9001/multi-demand?keyword=%D1%8E%D1%80%D0%B8%D0%B4%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8%D0%B9%20%D0%98%D0%98%20%D0%B4%D0%BB%D1%8F%20%D0%B8%D1%81%D0%BA%D0%BE%D0%B2 ; http://172.18.0.1:9001/multi-demand?keyword=%D1%81%D0%BE%D1%81%D1%82%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%B8%D1%81%D0%BA%D0%BE%D0%B2%20%D0%BE%D0%BD%D0%BB%D0%B0%D0%B9%D0%BD ; http://172.18.0.1:9001/multi-demand?keyword=%D0%B0%D0%B2%D1%82%D0%BE%D0%BC%D0%B0%D1%82%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F%20%D1%8E%D1%80%D0%B8%D0%B4%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8%D1%85%20%D0%B4%D0%BE%D0%BA%D1%83%D0%BC%D0%B5%D0%BD%D1%82%D0%BE%D0%B2]
- **Решение по гейту**: **EARLY REJECT**. Demand = LOW, и ни один из реалистичных сценариев монетизации не показывает убедимый путь к **EBITDA >= 500 тыс. ₽/мес** на российском plaintiff-personal-injury wedge без дорогого сервиса, длинного внедрения и ухода в соседний enterprise-сегмент. [T1/T2, inference]

## Evidence of demand

### 1) Mandatory endpoint
- `юридический ИИ для исков` → **LOW**, score **3**, `hh_vacancies = 16`, `yandex_suggest = 2`. [T2: internal demand endpoint]
- `составление исков онлайн` → **LOW**, score **3**, `hh_vacancies = 39`, `yandex_suggest = 2`. [T2: internal demand endpoint]
- `автоматизация юридических документов` → **LOW**, score **15**, `hh_vacancies = 554`, `yandex_suggest = 2`. Это уже более широкий adjacent pain, а не прямой personal injury wedge. [T2: internal demand endpoint]
- Вывод: спрос на юридическую автоматизацию в широком смысле существует, но именно plaintiff-side personal injury AI в РФ пока не сформирован как category demand. [T2, inference]

### 2) Дополнительные рыночные сигналы
- Росстат оценивает объем платных **юридических услуг населению** в РФ за **2024** год в **164 958,6 млн ₽**. Это подтверждает существование денежного рынка legal services, но не рынка software для plaintiff firms. [T1: https://rosstat.gov.ru/storage/mediabank/plat_usl_2024.xlsx]
- Судебный департамент при Верховном Суде РФ за **2024** год зафиксировал в районных судах **125,9 тыс.** дел о возмещении ущерба от ДТП и **122,5 тыс.** дел по спорам из нарушений законодательства о страховании. Эти категории близки к personal injury / insurance-claims workflow и показывают, что релевантный поток дел есть, но он намного уже всего юридического рынка. [T1: https://www.cdep.ru/index.php?id=79&item=9243]
- Правовед заявляет более **40 000 юристов** в сети и более **2,2 млн** клиентов/обращений, что подтверждает массовый B2C legal спрос в онлайне. Но это больше marketplace-консультации, а не специализированный plaintiff-operations SaaS. [T2: https://pravoved.ru/]
- Следовательно, денежный legal market в РФ реален, однако direct transfer американского motion EvenUp в локальный plaintiff-side сегмент плохо подтвержден. [T1/T2, inference]

## Real competitors with prices
1. **Clio**, глобальный legal practice management competitor: **$49/user/mo** на annual и **$59/user/mo** на monthly для EasyStart. Это нижняя граница WTP за legal workflow software. [T2: https://www.clio.com/pricing/]
2. **PracticePanther**: публичные планы от **$49** до **$114/user/mo** на annual. [T2: https://www.practicepanther.com/pricing/]
3. **Smokeball**: публично заявляет цену **from $149/mo**. [T2: https://www.smokeball.com/pricing/]

### Что это значит для РФ
- Эти конкуренты подтверждают, что на зрелых англоязычных рынках юридические команды платят за workflow software. [T2]
- Но для российского plaintiff-personal-injury wedge эти цены не являются прямым переносом, потому что локальные фирмы обычно меньше, менее стандартизированы и чаще покупают услугу, а не software seat. [T1/T2, inference]

## Telegram bots / services in RU
- Mandatory endpoint по legal-AI keywords не показывает заметного Telegram-сигнала, в ответах сервиса `telegram subscribers = 0`. [T2: internal demand endpoint]
- **Pravoved / pravorobot** существует как Telegram legal-touchpoint для быстрых консультаций. Это полезный B2C канал, но не доказательство B2B workflow demand. [T2: https://botostore.com/c/pravorobot/]
- **TeleTips** продает инфраструктуру платных консультаций в Telegram по тарифам **250 ₽/мес**, **600 ₽/мес** и **1000 ₽/мес**; среди примеров использования есть юристы. Это подтверждает, что Telegram monetizable как канал консультаций, но чеки там на порядки ниже venture-grade legal workflow SaaS. [T2: https://teletips.ru/]
- Вывод: в РФ Telegram подходит как intake/leadgen/консультации, но не выглядит ядром standalone plaintiff-claims platform. [T2, inference]

## WTP, willingness to pay
- **Есть WTP за legal outcome/service, а не за узкий plaintiff AI-product**: рынок платных юруслуг населению в 2024 году составил **164,96 млрд ₽**, а large online legal marketplace существует. [T1/T2]
- **Есть WTP за software на зрелых рынках**: Clio, PracticePanther и Smokeball имеют публичные цены, значит юридические команды платят за workflow. [T2]
- **Но локальное WTP в российском plaintiff wedge слабое**: в обязательном demand endpoint по близким формулировкам спрос LOW, Telegram monetization низкочековая, а основной local spend часто уходит в разовые услуги по подготовке иска/консультации, а не в recurring SaaS. [T2, inference]
- Итог: **proof of willingness to pay = частичный**. За юридическую помощь и общий legaltech платят, но прямого сильного доказательства recurring WTP именно за plaintiff-personal-injury AI в РФ нет. [T1/T2]

## Market sizing

### Методика и допущения
- Базовый денежный верхний уровень в РФ: **164,96 млрд ₽** юридических услуг населению за 2024 год. [T1]
- Адресуемый wedge для EvenUp-подобного motion связываем с делами по ДТП и страховым спорам: **125,9 тыс. + 122,5 тыс. = 248,4 тыс.** релевантных дел в 2024 году. [T1]
- Средний реалистичный software-чек для небольшой/средней юрфирмы в РФ берем на уровне **300 тыс. ₽ ARR** на фирму, то есть **25 тыс. ₽/мес**. Это уже заметный, но не агрессивный чек для узкого специализированного инструмента. [T2, inference]
- Для bottom-up считаем, что реально пригодных для покупки фирм в beachhead-сегменте около **300** по РФ, из них pain достаточно выражен у **60%**. Это оценка по рынку специализированных практик по ДТП, страховым спорам и consumer litigation; точного официального реестра нет, поэтому секция помечена как оценочная. [T2/T3, inference]

### Top-down
- **TAM (мир)**: reliable global baseline по именно plaintiff personal injury AI разнороден; для принятия решения используем РФ и не опираемся на глобальную цифру. [T3/speculation]
- После cross-check с bottom-up адресуемую долю внутри рынка платных юруслуг понижаем до **0,036%** от общего рынка, потому что продукт подходит только очень узкому слою plaintiff/insurance-litigation практик, а не всему legal services market. [T1/T2, inference]
- **TAM (РФ)** = **164,96 млрд ₽ × 0,036%** = **59,4 млн ₽**. [T1/T2, inference]
- **SAM (РФ)** = **59,4 млн ₽ × 88,9%** = **52,8 млн ₽**. Это software-ready часть узкого beachhead-сегмента. [T1/T2, inference]
- **SOM Y1** = **52,8 млн ₽ × 6,8%** = **3,6 млн ₽**. [inference]
- **SOM Y3** = **52,8 млн ₽ × 22,7%** = **12,0 млн ₽**. Значение выглядит агрессивно, но в абсолютных рублях все равно мало и не меняет reject-вывод. [inference]

### Bottom-up
- **Total buyers** = **300** специализированных или близких к сегменту юрфирм/практик. [T2/T3, inference]
- **% with need** = **60%**. [T2/T3, inference]
- **ARR avg** = **300 тыс. ₽/год**. [T2, inference]
- **SAM bottom-up** = **300 × 60% × 300 тыс. ₽ = 54,0 млн ₽**. [inference]
- **SOM bottom-up Y1** = **12 клиентов × 300 тыс. ₽ = 3,6 млн ₽**. [inference]
- **SOM bottom-up Y3** = **40 клиентов × 300 тыс. ₽ = 12,0 млн ₽**. [inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | н/д [T3] | — | reliable baseline нет | — |
| TAM (РФ) | 59,4 млн ₽ [T1/T2] | 54,0 млн ₽* [T2/T3] | diff=10,0%, оценки близки после пересмотра адресуемой доли | lower |
| SAM (РФ) | 52,8 млн ₽ [T1/T2] | 54,0 млн ₽ [T2/T3] | diff=2,2%, оценки сошлись | lower |
| SOM Y1 | 3,6 млн ₽ | 3,6 млн ₽ | diff=0%, используем консервативную общую цифру | **используем 3,6 млн ₽** |
| SOM Y3 | 12,0 млн ₽ | 12,0 млн ₽ | diff=0%, используем общую цифру | **используем 12,0 млн ₽** |

\* Для узкого wedge bottom-up TAM практически совпадает с SAM beachhead, потому что далеко не весь рынок юридических услуг software-ready.

### GTM 10 real buyers for bottom-up sanity check
1. **Европейская Юридическая Служба**. [T2: https://els24.com/]
2. **Правокард**. [T2: https://pravocard.ru/]
3. **Правовед.ру**. [T2: https://pravoved.ru/]
4. **Бизнес-Юрист**. [T2: https://biznes-yurist.ru/]
5. **Автоюрист**. [T3: https://avtourist.info/]
6. **Центр помощи при ДТП**. [T3: https://xn--d1aciiaf4a3f.xn--p1ai/]
7. **Возврат страховок**. [T3: https://vzrashod.ru/]
8. **Юрист для Людей**. [T2: https://юрпомощь.рф/]
9. **DestraLegal**. [T2: https://destralegal.ru/]
10. **Platforma**. [T2: https://platforma-online.ru/]

Sanity check: при цикле сделки **3-6 месяцев** и чеке **300 тыс. ₽ ARR** для достижения даже **SOM Y1 = 3,6 млн ₽** нужно закрыть **12 клиентов** за год. Для узкого сегмента это уже напряженно, а до venture-level масштаба далеко. [T2/T3, inference]

## Profit Gate: проверка всех сценариев монетизации

### Сценарий A. Self-serve SaaS для юрфирм
- При чеке **25 тыс. ₽ MRR** на фирму нужно не менее **20 платящих фирм**, чтобы получить лишь **500 тыс. ₽ выручки в месяц**, еще до учета команды, модели и поддержки. [inference]
- Для EBITDA **500 тыс. ₽/мес** потребовалось бы значительно больше клиентов или намного более высокий чек, что плохо сочетается с LOW demand. [T2, inference]
- **Вердикт: FAIL.**

### Сценарий B. Плата за документ / иск
- Если брать **1-3 тыс. ₽** за документ, понадобится сотни и тысячи транзакций в месяц. Это превращает бизнес в сервисный high-volume B2C/B2B2C с дорогим acquisition. [T2/T3, inference]
- **Вердикт: FAIL.**

### Сценарий C. Managed service для plaintiff firms
- Можно поднять чек, добавив human review и внедрение, но тогда экономика уходит из software в labor-heavy legal ops. [T1/T2, inference]
- При узком сегменте и длинной адаптации это не дает чистой software EBITDA >= 500 тыс. ₽/мес без значимой команды. [T1/T2, inference]
- **Вердикт: FAIL.**

### Сценарий D. Telegram-first bot
- Telegram monetization в legal консультациях существует, но рыночные ориентиры вроде **250-1000 ₽/мес** у TeleTips слишком низки для фонда уровня software business. [T2]
- **Вердикт: FAIL.**

## Risks
- Российский plaintiff-personal-injury рынок структурно слабее американского EvenUp wedge. [T1/T2, inference]
- Buyers фрагментированы, часто покупают услугу, а не recurring software. [T2, inference]
- Для успеха пришлось бы смещаться в соседний enterprise claims/legal-ops сегмент, то есть фактически менять исходный wedge. [T1/T2, inference]

## Verdict for P4
- **P4 verdict**: **REJECTED**.
- Причина: **DEMAND = LOW** по обязательному endpoint, а **Profit Gate FAIL** во всех проверенных сценариях монетизации для исходного plaintiff-personal-injury motion в РФ. [T1/T2]
- Отдельно: кейс концептуально ближе к уже существующему более широкому направлению claims/legal-ops automation, но как standalone российский plaintiff-PI GEO-expand wedge не проходит. [T1/T2, inference]

Sources: T1=4, T2=18, T3=5. Primary evidence basis: T2.
