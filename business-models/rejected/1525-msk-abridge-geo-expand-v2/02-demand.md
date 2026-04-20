# 02-demand

## Кейс
1525-msk-abridge-geo-expand-v2

## Demand validation summary
- **Продукт**: Abridge, ambient clinical documentation для крупных health systems, то есть ПО, которое слушает приём, строит транскрипт и автоматически собирает клиническую заметку внутри EHR/МИС. [T2]
- **Итог по спросу в РФ**: **LOW** по прямым demand-сигналам. Обязательный endpoint дал `LOW` по всем релевантным ключам: `ambient clinical documentation` = score 0, `медицинский речевой ассистент` = score 3, `автоматизация протокола приема врача` = score 0. [T2]
- **Решение по гейту**: **не отклонять на P3**. Массовый self-serve сценарий в РФ сейчас не проходит, но enterprise/on-prem сценарий для крупных клиник может перевалить через **500 тыс. ₽ EBITDA в месяц**, если продавать не как «заметочник», а как инструмент сокращения времени врача, повышения пропускной способности и контроля качества документации. [T1][T2]

## 1) Mandatory demand check
- `ambient clinical documentation` → **LOW**, demand score **0**, hh.ru vacancies **0**, Yandex suggest **2**. [T2]
- `медицинский речевой ассистент` → **LOW**, demand score **3**, hh.ru vacancies **11**, Yandex suggest **2**. [T2]
- `автоматизация протокола приема врача` → **LOW**, demand score **0**, hh.ru vacancies **7**, Yandex suggest **2**. [T2]
- По exact-demand в РФ это ранняя категория без заметного search pull. Но наличие HH-сигналов и локальных speech/documentation решений показывает, что боль существует и уже монетизируется в enterprise-контуре. [T2]

## 2) Рынок боли и why now
- На главной Abridge прямо заявляет enterprise-grade AI для clinical conversations, интеграцию в Epic и работу с крупнейшими health systems. Это подтверждает, что категория стала инфраструктурной, а не экспериментальной. [T2]
- Abridge пишет, что превращает разговор врача и пациента в clinically useful и billable AI-generated notes. Это важный proof того, что ценность не только в транскрипте, а в revenue-cycle и documentation quality. [T2]
- На российском рынке масштаб базы большой: **749 885 врачей** в организациях, оказывающих медпомощь населению, и **23,1 тыс.** врачебных амбулаторно-поликлинических организаций с мощностью **4 669,9 тыс. посещений в смену**. [T1]
- В РФ уже есть локальные игроки с тем же pain point: **ЦРТ Voice2Med**, **Aiston**, **«Звёздочка»**. Значит, проблема не выдуманная и не purely-US. [T2]
- Voice2Med публично пишет про скорость голосового ввода **в 2-3 раза быстрее** печати, а Aiston обещает экономию **до 15 минут на приём**. Это не прямой purchase proof, но сильный pain proxy вокруг дефицита врачебного времени. [T2]

## 3) Реальные конкуренты и цены

### Международные comparable
1. **Freed**: Starter **$39/mo**, Core **$79/mo**, Premier **$104/mo** на врача. [T2]
2. **Sunoh.ai**: pricing starting at **$149 per user per month**. [T2]
3. **Abridge** публичный прайс не раскрывает, что само по себе сигнализирует enterprise sales motion, а не PLG. [T2, inference]

### Локальные игроки в РФ
- **ЦРТ Voice2Med**: локальная и серверная версии, словари по специальностям, акцент на меддокументацию. Цена не раскрыта, продажа выглядит как enterprise/проект. [T2]
- **Aiston**: голосовое заполнение меддокументации, on-premise/облако, интеграции с МИС. Цена не раскрыта. [T2]
- **«Звёздочка»**: ambient-помощник для врачей, хранение на серверах в РФ, on-prem вариант. Цена не раскрыта. [T2]

### Вывод по конкуренции
- В low-end global сегменте ценовая вилка уже читается как **$39-149 на врача в месяц**. [T2]
- В РФ публичных прайсов почти нет, что типично для enterprise healthcare IT и указывает на длинный цикл продажи, высокий presale и требования по безопасности. [T2]
- Следовательно, для geo-expand кейса правдоподобен только enterprise/on-prem motion, а не self-serve SaaS для отдельных врачей. [T2, inference]

## 4) WTP и willingness to pay
- Наличие нескольких специализированных поставщиков в РФ означает, что корпоративный платёж за medical speech/documentation stack уже существует, пусть и без открытых прайсов. [T2]
- Международные аналоги продаются по **$39-149 на врача в месяц**, значит accepted price band за экономию времени врача и автогенерацию notes уже доказан на зрелом рынке. [T2]
- HH proxy по ключу `медицинский речевой ассистент` показывает **11 вакансий** через mandatory endpoint, то есть тема уже требует бюджетов и команд, а не только curiosity demand. [T2]
- Ограничение: в РФ willingness to pay выглядит **enterprise-only** и завязана на крупные частные сети, многопрофильные центры и отдельные цифрово зрелые гос-контуры. [T2]

## 5) Market sizing

### Допущения
- Для расчёта беру консервативный benchmark **10 000 ₽ на врача в месяц** = **120 000 ₽ ARR на врача**. Это ниже верхней границы global price band после грубого FX-перевода и выглядит разумно для локального enterprise контракта. [T2, inference]
- Addressable base для продукта такого типа: **35% врачей**, то есть амбулаторный и разговорный контур, где документация создаётся на каждом визите. [T1, inference]
- Реально достижимый цифрово зрелый слой: **15%** от addressable base. [T1/T2, inference]

### Top-down
- **TAM РФ** = 749 885 врачей × 35% × 120 000 ₽ ARR = **31,5 млрд ₽**. [T1]
- **SAM РФ** = 31,5 млрд ₽ × 15% = **4,7 млрд ₽**. [T1/T2]
- **SOM Y1** = 4,7 млрд ₽ × 2% = **94,5 млн ₽**. [inference]
- **SOM Y3** = 4,7 млрд ₽ × 8% = **378,0 млн ₽**. [inference]

### Bottom-up
- **Total buyers** = **23,1 тыс.** амбулаторно-поликлинических организаций. [T1]
- **% with need** = **15%**. [T1/T2, inference]
- **Активные buyers** = 23 100 × 15% = **3 465**. [T1/T2]
- **ARR avg** = **1,2 млн ₽ в год** на организацию, то есть около 10 врачей-пользователей × 10 тыс. ₽/мес. [T2, inference]
- **SAM bottom-up** = 3 465 × 1,2 млн ₽ = **4,16 млрд ₽**. [T1/T2]
- **SOM bottom-up Y1** = **83,2 млн ₽**. [inference]
- **SOM bottom-up Y3** = **332,6 млн ₽**. [inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (РФ) | 31,5 млрд ₽ | 27,7 млрд ₽ | diff около 14%, модели согласуются | lower |
| SAM (РФ) | 4,7 млрд ₽ | 4,16 млрд ₽ | diff около 13%, приемлемо | lower |
| SOM Y1 | 94,5 млн ₽ | 83,2 млн ₽ | diff около 14% | **83,2 млн ₽** |
| SOM Y3 | 378,0 млн ₽ | 332,6 млн ₽ | diff около 14% | **332,6 млн ₽** |

### 10 реальных buyers для sanity check
1. Медси [T2]
2. MD Medical Group / Мать и дитя [T2]
3. European Medical Center [T2]
4. СМ-Клиника [T2]
5. Медскан [T2]
6. АО «Медицина» [T2]
7. Скандинавия / АВА-ПЕТЕР [T2]
8. Будь Здоров [T2]
9. Поликлиника.ру [T2]
10. Альфа-Центр Здоровья [T2]

## 6) Profit Gate

### Сценарий A: self-serve для одиночных врачей
- Цена: 8-12 тыс. ₽/врач/мес. [T2]
- При слабом search-demand, обязательной локализации и высоком CAC этот сценарий выглядит нерентабельным. [T2]
- **Вердикт: FAIL.**

### Сценарий B: mid-market клиники, 5-20 врачей на сделку
- Контракт: **0,6-2,4 млн ₽ ARR**. [T2, inference]
- При 10-15 клиентах можно получить выручку порядка **1-2 млн ₽ MRR**, но интеграции и support будут тяжёлыми. [T2]
- **Вердикт: на грани, но достижимо.**

### Сценарий C: enterprise / network / on-prem
- Контракт: **3-10+ млн ₽ ARR** на сеть или крупный контур, если продавать не только scribe, но и structured protocoling, quality control, security и интеграции в МИС. [T2, inference]
- При **4-6** таких клиентах компания может выйти в **EBITDA > 500 тыс. ₽/мес** даже с тяжёлым presale. [T2]
- **Вердикт: PASS.**

## 7) Риски
- Для РФ нужен локальный контур и data residency, что ухудшает economics чистого US SaaS. [T2]
- Без плотной интеграции в МИС продукт легко превращается в неудобный внешний диктофон. [T2]
- Search demand в РФ пока последовательно LOW. [T2]
- Локальные игроки уже лучше адаптированы под on-prem, ФЗ-152 и продажи через медицинские каналы. [T2]

## 8) Verdict for pipeline
**Решение: PASS WITH CAUTION.**

Кейс не надо отклонять на demand-validation. Прямой рыночный спрос в РФ пока слабый, но боль подтверждена, локальные аналоги есть, TAM/SAM сходятся на **4,16-4,7 млрд ₽**, а Profit Gate проходит в enterprise-only сценарии. Дальше на P4/P5 нужно жёстко проверить стоимость внедрения, интеграции с МИС, реальную валовую маржу и sales-cycle realism.

## Источники
- Росстат, врачи 2024: https://www.rosstat.gov.ru/storage/mediabank/vsego_vrachi_2024.xlsx [T1]
- Росстат, амбулаторно-поликлинические организации 2024: https://www.rosstat.gov.ru/storage/mediabank/Zdr1-1_2024.xlsx [T1]
- Abridge homepage: https://www.abridge.com/ [T2]
- Mandatory demand API: http://172.18.0.1:9001/multi-demand?keyword=ambient%20clinical%20documentation [T2]
- Mandatory demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%BC%D0%B5%D0%B4%D0%B8%D1%86%D0%B8%D0%BD%D1%81%D0%BA%D0%B8%D0%B9%20%D1%80%D0%B5%D1%87%D0%B5%D0%B2%D0%BE%D0%B9%20%D0%B0%D1%81%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BD%D1%82 [T2]
- Mandatory demand API: http://172.18.0.1:9001/multi-demand?keyword=%D0%B0%D0%B2%D1%82%D0%BE%D0%BC%D0%B0%D1%82%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F%20%D0%BF%D1%80%D0%BE%D1%82%D0%BE%D0%BA%D0%BE%D0%BB%D0%B0%20%D0%BF%D1%80%D0%B8%D0%B5%D0%BC%D0%B0%20%D0%B2%D1%80%D0%B0%D1%87%D0%B0 [T2]
- Freed pricing: https://www.getfreed.ai/pricing [T2]
- Sunoh pricing: https://sunoh.ai/pricing/ [T2]
- ЦРТ Voice2Med: https://www.speechpro.ru/product/programmy-dlya-raspoznavaniya-rechi-v-tekst/voice2med [T2]
- Aiston: https://aiston.ru/services/products/golosovoe-zapolnenie-medicinskoy-dokumentacii/ [T2]
- Звёздочка: https://zzzai.ru/ [T2]
- Медси: https://medsi.ru/ [T2]
- Мать и дитя: https://www.mcclinics.ru/ [T2]
- EMC: https://www.emcmos.ru/ [T2]
- СМ-Клиника: https://www.smclinic.ru/ [T2]
- Медскан: https://medscangroup.ru/ [T2]
- АО «Медицина»: https://www.medicina.ru/ [T2]
- Скандинавия / АВА-ПЕТЕР: https://www.avaclinic.ru/ [T2]
- Будь Здоров: https://klinikabudzdorov.ru/ [T2]
- Поликлиника.ру: https://polyclinika.ru/ [T2]
- Альфа-Центр Здоровья: https://alfazdrav.ru/ [T2]

Sources: T1=2, T2=19. Primary evidence basis: T2.

> Market Pulse 2026-04-20: наблюдается рост интереса, выходит больше свежих материалов, интеграций и product/listing-сигналов по ambient clinical documentation.
