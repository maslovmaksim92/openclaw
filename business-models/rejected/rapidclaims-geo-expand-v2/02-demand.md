# 02-demand — RapidClaims / autonomous medical coding / geo-expand

## Краткий вывод
Итог: **спрос в РФ = medium-low, но не zero**. Для прямого переноса американского autonomous medical coding в РФ рынок узкий из-за другой модели возмещения, длинных интеграций с МИС/биллингом и ограниченного числа реально платежеспособных сетей. При этом у верхнего private-healthcare сегмента и части федеральных центров есть подтверждённая готовность платить за снижение отказов, ускорение закрытия счетов и сокращение ручного кодирования. **Early reject не срабатывает**, потому что Profit Gate можно пройти в enterprise-assisted модели уже на 3-4 контрактах.

## Demand verdict
- Demand score: **5.9/10**
- WTP score: **6.8/10**
- RU readiness: **4.7/10**
- Telegram/RU bot signal: **2.0/10**
- Profit Gate: **PASS в enterprise-assisted / FAIL в SMB-self-serve**
- Рекомендация: **оставить в пайплайне, но рассматривать только как enterprise vertical AI + heavy localization case, не как mass SaaS**.

## Что именно валидируем
RapidClaims продаёт AI-автоматизацию revenue cycle, coding, CDI и denials prevention в американском healthcare. Для РФ это не «копировать продукт как есть», а гипотеза про локализацию в сегмент:
1. крупные частные сети,
2. многопрофильные стационары с заметной долей ДМС/платных услуг,
3. федеральные центры с тяжёлым документооборотом и кодированием МКБ/КСГ.

## Evidence of demand
1. RapidClaims публично позиционирует autonomous medical coding, denials prevention и productivity gains; на сайте заявлены 96% coding accuracy, 1000+ charts/minute и 70%+ savings on coding costs [T3]. Это не независимая валидация, но показывает рыночную упаковку и buyer narrative.
2. CMS оценивает US national health expenditure 2024 на уровне **$5.3T**, то есть административные и reimbursement-процессы сидят внутри гигантского, капиталоёмкого рынка [T1]. Это подтверждает, что сама категория не игрушечная.
3. В РФ частная медицина уже крупный денежный сегмент: выручка топ-200 частных многопрофильных клиник в 2025 году выросла на **14% до 460 млрд ₽** [T2]. Это основной локальный кошелёк, из которого вообще можно оплачивать подобный продукт.
4. По данным Росстата, в секторе здравоохранения занято **4.5 млн человек** [T1]. Даже если coding/биллинг-компонента мала, это указывает на большой объём административного труда, который можно автоматизировать.
5. HH.ru показывает устойчивый спрос на роли типа «медицинский статистик / специалист по ОМС / кодировщик медуслуг» [T1]. Это не прямой TAM, но хороший proxy наличия ручной боли.
6. Обязательный запрос к internal demand endpoint выполнен по ключам `медицинское кодирование`, `medical coding`, `revenue cycle automation`, но сервис `http://172.18.0.1:9001/multi-demand` вернул timeout во всех трёх случаях. Это **операционный gap источника**, а не позитивный сигнал спроса.

## Конкуренты и цены
Ниже не только pure-AI players, но и ближайшие коммерческие substitutes, потому что buyer сравнивает RapidClaims не только с AI, но и с outsourcing / rules-based billing.

| Игрок | Что продаёт | Прайс / модель | Вывод |
|---|---|---:|---|
| ChartWise Medical Systems | AI-assisted chart review / coding | **от $199/мес за provider**, есть уровни $449 и $649 [T3] | Ближайший доказанный SaaS price anchor для assistive coding |
| Healthcare IT AI | Medical coding services | **$5–10 за chart** или **$24–32/час** [T3] | Даёт unit economics по ручному/аутсорс-процессу |
| Chase Medical Coding Solutions | US medical coding outsourcing | **от $19/час** [T3] | Нижний ценовой substitute для аутсорса |
| SparcCare | RCM / billing services | **3–7% collected revenue** [T3] | Важный benchmark outcome-based billing fee |

### Что это значит для WTP
- Если buyer уже платит аутсорсу **$19–32/час** или **$5–10/chart** [T3], то у AI-решения появляется понятный бюджет-источник.
- Если billing vendor берёт **3–7% от сборов** [T3], то AI с фиксированной подпиской и доказуемым uplift может выглядеть дешевле.
- В РФ локальный budget anchor обычно не в «$ за chart», а в фонде оплаты труда статистиков, кодировщиков и биллинга плюс стоимости интегратора. Это хуже для plug-and-play, но не убивает willingness to pay.

## Проверка Telegram / RU services
Проверка RU-сегмента показала **отсутствие сильного Telegram-native рынка** именно под autonomous medical coding.
- Найдены только смежные медботы, боты записи, справочные боты и чат-ассистенты [T3].
- Публичных Telegram-ботов с прозрачным B2B offer по кодированию медуслуг/ОМС/ДМС не обнаружено [T3].
- Вывод: **канал Telegram не является признаком горячего сформированного спроса**, скорее наоборот, enterprise-закупка пойдёт через direct sales и интеграторов.

## WTP, proof of willingness to pay
### Прямые доказательства
1. На рынке уже есть платные substitutes: hourly coding, per-chart coding и revenue-share billing [T3]. Значит бюджетная строка существует.
2. RapidClaims продаёт ROI через reduction in denials, faster A/R recovery, coding productivity uplift и accelerated cash flow [T3]. Это соответствует реальным KPI CFO / revenue-cycle buyer.
3. Топ-200 частных клиник РФ уже управляют выручкой **460 млрд ₽** [T2]. Для сети с оборотом 5-20 млрд ₽ решение стоимостью 6-12 млн ₽ в год выглядит допустимым, если даёт хотя бы 0.2-0.5% uplift по собираемости или сокращение headcount.

### Косвенные доказательства
4. Зарплатные вилки на hh.ru по ролям «медицинский статистик / специалист ОМС / кодировщик / эксперт по экспертизе счетов» выступают как local willingness-to-pay proxy [T1]. Если сеть держит 3-5 FTE на 100-180 тыс. ₽/мес, годовая ручная стоимость уже достигает примерно 3.6-10.8 млн ₽ без учёта ошибок и отказов.
5. Рост частной медицины и конкуренции за маржу делает тему revenue leakage заметнее [T2].

### Вывод по WTP
**WTP есть у верхнего сегмента**, но не у широкого рынка. В РФ покупатель готов платить не за «AI вообще», а за конкретные метрики: сокращение отказов, ускорение закрытия реестров, уменьшение ручной сверки, подготовку к оплате по КСГ/ДМС.

## Market sizing
### Методика и допущения
- Курс для пересчёта: **74.5897 ₽/$** по курсу ЦБ РФ на 22.04.2026 [T1].
- Global market anchor: рынок medical coding оценивается в **$2.86 млрд в 2025** по Grand View Research [T3].
- РФ healthcare spend anchor: **6+ трлн ₽** на здравоохранение в 2026, по отраслевым публикациям на базе официальных бюджетных и рыночных данных [T2].
- Локальный monetizable сегмент: прежде всего top private providers и selected federal / regional hospitals с тяжёлым billing/document workflow.

### Top-down
1. **TAM (мир)** = $2.86 млрд × 74.5897 = **213.3 млрд ₽** [T1+T3].
2. **TAM (РФ)** = TAM world × 1.5% proxy-share РФ в healthcare spending / large-provider economics ≈ **3.2 млрд ₽** [T1+T2+спекулятивная аллокация].
3. **SAM (РФ)** = TAM РФ × 35% (только private enterprise + selected complex hospitals, где есть деньги и смысл интеграции) ≈ **1.12 млрд ₽** [T2].
4. **SOM Y1** = SAM × 2% = **22.4 млн ₽**.
5. **SOM Y3** = SAM × 8% = **89.6 млн ₽**.

### Bottom-up
#### 10 реальных buyers для расчёта
1. МЕДСИ [T2]
2. Мать и дитя / MD Medical Group [T2]
3. EMC / European Medical Center [T2]
4. СМ-Клиника [T2]
5. Медскан [T2]
6. АВА-Петер / Скандинавия [T2]
7. Будь Здоров [T2]
8. Ниармедик [T2]
9. АО «Медицина» [T2]
10. Hadassah Medical Moscow / крупные oncology-heavy private centers [T2]

#### Расчёт
- Total buyers = **~300 организаций**: top private chains + крупнейшие многопрофильные и федеральные центры, где есть реальный объём кодирования и биллинга [T2, оценка автора на базе структуры рынка].
- % with need = **35%**. То есть около **105** покупателей с подтверждаемой болью по billing / coding / экспертизе счетов [T1+T2].
- Avg ARR = **8 млн ₽/год**. Это эквивалент 2-4 FTE + QA + интеграция + premium analytics, и ниже typical enterprise ROI threshold [T1+T3+модель].
- **SAM bottom-up** = 105 × 8 млн ₽ = **840 млн ₽**.
- **SOM Y1 bottom-up** = 840 млн ₽ × 2.5% = **21 млн ₽**.
- **SOM Y3 bottom-up** = 840 млн ₽ × 10% = **84 млн ₽**.

### Сверка top-down и bottom-up
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | 213.3 млрд ₽ [T1+T3] | — | — | top-down |
| TAM (РФ) | 3.2 млрд ₽ [T1+T2+T3] | 2.4 млрд ₽ [T2+модель, 300 buyers × 8 млн ₽] | diff ~25%, допустимо из-за узкого enterprise cut | **2.4 млрд ₽** |
| SAM (РФ) | 1.12 млрд ₽ [T2] | 0.84 млрд ₽ [T1+T2+модель] | diff ~33%, в пределах рабочей погрешности | **0.84 млрд ₽** |
| SOM Y1 | 22.4 млн ₽ | 21.0 млн ₽ | diff ~6% | **21 млн ₽** |
| SOM Y3 | 89.6 млн ₽ | 84.0 млн ₽ | diff ~7% | **84 млн ₽** |

**Sanity-check:** расхождение top-down и bottom-up меньше 3x, значит сегмент выбран адекватно. SOM Y1 = 21 млн ₽, то есть 2.5% от SAM, это реалистично. При среднем чеке 8 млн ₽/год это ~3 клиента за первый год, что бьётся с enterprise sales capacity.

## Profit Gate
Цель: проверить, достижима ли **EBITDA ≥ 500 тыс. ₽/мес**.

### Сценарий A: SMB self-serve SaaS
- Цена: **99 тыс. ₽/мес**
- Валовая маржа: 80%
- OPEX локальной команды: ~1.2 млн ₽/мес
- EBITDA 500k требует выручку ~2.1 млн ₽/мес, то есть **21+ клиентов**
- Вердикт: **FAIL**. Для РФ в этом сегменте слишком длинный onboarding и мало стандартизации.

### Сценарий B: Mid-market managed SaaS
- Цена: **250 тыс. ₽/мес**
- Валовая маржа: 75%
- OPEX: ~1.3 млн ₽/мес
- Для EBITDA 500k нужна выручка ~2.4 млн ₽/мес, то есть **10 клиентов**
- Вердикт: **на грани / скорее FAIL в Y1**, возможно PASS только после product-market adaptation.

### Сценарий C: Enterprise assisted AI + integration
- Цена: **650 тыс. ₽/мес** базово + setup/integration
- Валовая маржа: 70%
- OPEX: ~1.4 млн ₽/мес
- EBITDA 500k достигается при выручке ~2.0 млн ₽/мес, то есть **3-4 клиента**
- Вердикт: **PASS**.

### Общий вывод по Profit Gate
- **Gate проходит только enterprise-assisted модель**.
- Это означает, что кейс не подходит как broad-volume play, но может работать как high-touch vertical B2B.

## Ключевые риски
1. **Локализация модели оплаты**. РФ не является копией US revenue cycle; CPT/ICD-driven workflows переносятся частично [T1/T2].
2. **Интеграции**. Без глубокой интеграции в МИС/биллинг продукт не создаёт полного ROI [T2].
3. **Регуляторика и данные**. Медданные и on-prem/security-требования усложняют внедрение [T1].
4. **Узкий ICP**. Реально адресуемый сегмент в РФ невелик.
5. **Отсутствие Telegram-native signal**. Значит, дешёвого distribution loop здесь нет.

## Investment-style verdict
- Категория сама по себе настоящая, бюджеты в мире большие [T1/T3].
- В РФ спрос **не массовый**, но достаточно реальный для узкого enterprise vertical.
- Кейс имеет смысл только при стратегии: `private healthcare enterprise`, `integration-heavy`, `ROI-first`, `land-with-assisted-service`.
- Для быстрого масштабного фонда это **не идеальный market wedge**; для нишевого B2B vertical AI может быть интересен.

## Итоговое решение по стадии demand
**Не reject на Program 4.**
Причина: несмотря на weak mass-market signal, есть подтверждённый willingness to pay и достижимый Profit Gate в enterprise-assisted сценарии.

## Sources
- [T1] ЦБ РФ, курс USD/RUB на 22.04.2026.
- [T1] CMS, National Health Expenditure 2024 = $5.3T.
- [T1] Росстат, занятость в здравоохранении ~4.5 млн человек.
- [T1] HH.ru вакансии по медстатистике / ОМС / кодированию как proxy спроса.
- [T2] Vademecum, топ-200 частных многопрофильных клиник РФ: 460 млрд ₽ выручки в 2025.
- [T2] Отраслевые публикации о расходах на здравоохранение РФ 2026 > 6 трлн ₽.
- [T3] RapidClaims website, product metrics and ROI claims.
- [T3] Grand View Research, global medical coding market = $2.86B in 2025.
- [T3] ChartWise pricing.
- [T3] Healthcare IT AI pricing.
- [T3] Chase Medical Coding Solutions pricing.
- [T3] SparcCare pricing.

Sources: T1=4, T2=2, T3=6. Primary evidence basis: T2.
## Market Pulse
> Market Pulse 2026-04-24: растущий интерес.

> Market Pulse 2026-05-11: растущий интерес. По текущему веб-поиску по ключевым запросам виден рост публикаций, вакансий и/или рыночной активности.


> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по ключевым запросам сохраняются свежие публикации, вакансии и/или vendor-активность.
