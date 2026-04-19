# Demand Validation — AI-native Salesforce Implementation Operator

**Дата:** 2026-04-19 22:37 MSK
**Итог P4:** **DEMAND = LOW**, **Profit Gate = FAIL**, **ранний вердикт = REJECTED**.

## 1) Executive summary
- В РФ спрос на Salesforce-специалистов и внедрение есть только как остаточный niche demand, а не как растущий локальный рынок: mandatory endpoint дал `LOW` по всем ключевым запросам, включая `Salesforce`, `Agentforce` и `Salesforce implementation` [T2].
- Локальный рынок подрезан vendor-risk: Salesforce ещё в 2022 году приостановила продажи в России, а Slack в 2023 году деактивировал аккаунты российских пользователей, что снижает вероятность новых enterprise rollout'ов в РФ [T2].
- WTP у международных покупателей высокий, но это подтверждает скорее global/offshore consulting market, а не повторяемый рынок РФ [T2].
- Для фонда важен достижимый EBITDA >= 500K ₽/мес. В РФ-сегменте это не подтверждается ни в project-only, ни в retainer, ни в training/advisory сценарии [T1][T2].

## 2) Demand signals
### Mandatory multi-demand endpoint
- `Salesforce` -> demand_score 23, composite_demand `LOW`, hh_vacancies 55, Google Trends RU 3/100 [T2].
- `Agentforce` -> demand_score 15, composite_demand `LOW`, hh_vacancies 2, Google Trends RU 0/100 [T2].
- `Salesforce implementation` -> demand_score 0, composite_demand `LOW`, hh_vacancies 2, Google Trends RU 0/100 [T2].
- `Salesforce consulting` -> demand_score 3, composite_demand `LOW`, hh_vacancies 10, Google Trends RU 0/100 [T2].

### Hiring / market activity
- По поиску hh.ru на запрос `Salesforce` найдено 103 вакансии, но это уже весь широкий хвост, включая developer/admin/CRM manager и международные роли; для `salesforce developer` выдача показывает 27 вакансий в Москве [T1].
- В сниппетах hh.ru как работодатели фигурируют Банк ВТБ, Совкомбанк, билайн, ФосАгро, Johnson & Johnson, РСХБ-Интех, VK, YADRO, Dr. Reddy’s, GET Experts Recruitment [T1]. Это подтверждает наличие installed base, но не подтверждает новый массовый рынок внедрения [T1].
- Reuters сообщал, что Salesforce остановила бизнес в России в марте 2022 года, а TechCrunch писал, что Slack начал деактивацию аккаунтов российских пользователей в 2023 году [T2]. Для enterprise buyer это structural drag, а не временная флуктуация [T2].

## 3) Конкуренты и цены
Ниже референсы по реальным Salesforce implementation-партнёрам с открытыми ценовыми ориентирами. Конвертация в рубли сделана по курсу ЦБ РФ 76.0535 ₽/$ на 18.04.2026 [T1].

| Конкурент | Прайс | Min project | Что доказывает |
|---|---:|---:|---|
| Simplus (Clutch) | $200-300/ч = 15 211-22 816 ₽/ч [T2][T1] | от $10 000 = от 760 535 ₽ [T2][T1] | Enterprise buyer реально платит premium за Salesforce delivery |
| CloudMasonry (Clutch) | $200-300/ч = 15 211-22 816 ₽/ч [T2][T1] | от $5 000 = от 380 268 ₽ [T2][T1] | Даже базовые engagement'ы стоят сотни тысяч рублей |
| Go Nimbly (Clutch) | $150-199/ч = 11 408-15 135 ₽/ч [T2][T1] | от $50 000 = от 3 802 675 ₽ [T2][T1] | Большие transformation-проекты имеют multi-million budget |
| Peeklogic (Clutch) | $25-49/ч = 1 901-3 727 ₽/ч [T2][T1] | от $1 000 = от 76 054 ₽ [T2][T1] | Нижняя граница рынка для offshore staffing/implementation |

**Вывод по WTP:** willingness to pay подтверждён, но это WTP глобального Salesforce-рынка, а не сильного локального РФ demand pool [T2].

## 4) Telegram bots / services в РФ
- У Wazzup есть интеграция Salesforce + WhatsApp/Instagram, тарифы стартуют от 500 ₽/мес за канал, но это messaging connector, а не AI-native implementation operator [T2].
- Поисковая выдача по RU-сегменту показывает Albato, Wazzup и интеграторские статьи, но не показывает заметного пласта Telegram-ботов/сервисов именно под Salesforce Agentforce implementation в РФ [T2][T3].
- Вывод: Telegram/ботовый слой в РФ есть только как вспомогательная интеграционная инфраструктура. Отдельного спросового кластера под новый Salesforce-operator в РФ не видно [T2].

## 5) Market sizing
### Подход и допущения
- База для top-down: рынок CRM в России 44.1 млрд ₽ в 2024 году по TAdviser [T2].
- Addressable share для Salesforce-specific implementation взят на уровне 0.2% от CRM-рынка, потому что vendor уже ограничил присутствие в РФ, а hh-поиск показывает только 103 вакансии по широкому запросу `Salesforce` и 27 вакансий по `salesforce developer` [T1][T2].
- База для bottom-up: ориентир 40 организаций в РФ/с российскими командами, где Salesforce ещё поддерживается или упоминается в найме; из них 10 реальных buyer examples перечислены ниже [T1].

### 10 реальных buyers / target accounts для bottom-up
1. Банк ВТБ [T1]
2. Совкомбанк [T1]
3. билайн [T1]
4. ФосАгро [T1]
5. Johnson & Johnson [T1]
6. РСХБ-Интех [T1]
7. VK [T1]
8. YADRO [T1]
9. Dr. Reddy’s [T1]
10. GET Experts Recruitment [T1]

### Расчёт top-down
- **TAM (РФ)** = 44.1 млрд ₽ × 0.2% = **88.2 млн ₽** [T2][T1].
- **SAM (РФ)** = 88.2 млн ₽ × 70% enterprise/managed-optimization fit = **61.7 млн ₽** [T2][T1].
- **SOM Y1** = 61.7 млн ₽ × 8% realistic capture = **4.9 млн ₽** [T2].
- **SOM Y3** = 61.7 млн ₽ × 16% realistic capture = **9.9 млн ₽** [T2].

### Расчёт bottom-up
- **Total buyers** = 40 организаций с остаточной Salesforce-footprint в РФ [T1][T2].
- **% with need** = 60% нуждаются не просто в support, а в project/optimization work = 24 buyer'а [T1][T2].
- **ARR avg** = 2.5 млн ₽/год на hybrid engagement (разовый проект + небольшой retainer), выведено из открытых competitor minimums и укороченного РФ-бюджета [T2].
- **TAM (РФ, bottom-up)** = 40 × 2.5 млн ₽ = **100.0 млн ₽** [T1][T2].
- **SAM (РФ, bottom-up)** = 24 × 2.5 млн ₽ = **60.0 млн ₽** [T1][T2].
- **SOM Y1 (bottom-up)** = 2 клиента × 2.5 млн ₽ = **5.0 млн ₽** [T2].
- **SOM Y3 (bottom-up)** = 4 клиента × 2.5 млн ₽ = **10.0 млн ₽** [T2].

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | Salesforce FY25 revenue $37.9B = ~2.88 трлн ₽, implementation-layer addressable явно большой, но для этого кейса нерелевантен локальному gate [T1] | — | — | top-down |
| TAM (РФ) | 88.2 млн ₽ [T2][T1] | 100.0 млн ₽ [T1][T2] | diff=13.4%, оценки согласуются | **88.2 млн ₽** |
| SAM (РФ) | 61.7 млн ₽ [T2][T1] | 60.0 млн ₽ [T1][T2] | diff=2.8%, оценки согласуются | **60.0 млн ₽** |
| SOM Y1 | 4.9 млн ₽ [T2] | 5.0 млн ₽ [T2] | diff=2.0% | **5.0 млн ₽** |
| SOM Y3 | 9.9 млн ₽ [T2] | 10.0 млн ₽ [T2] | diff=1.0% | **10.0 млн ₽** |

### Sanity checks
- Расхождение между top-down и bottom-up меньше 3x, пересчёт согласован [T1][T2].
- SOM Y1 < 10% SAM, значит захват не overclaimed [T2].
- Даже при 2 клиентах в год рынок остаётся too thin для быстрого scale-up до фонда [T2].

## 6) WTP proof
- Высокий enterprise WTP подтверждают открытые рейты Simplus, CloudMasonry, Go Nimbly и Peeklogic: buyer уже покупает Salesforce delivery по ставкам от ~1.9k до ~22.8k ₽/ч [T2][T1].
- Но willingness to pay не равен доступному спросу в РФ. Здесь проблема не в цене, а в том, что локальный buyer pool слишком маленький и vendor-risk высокий [T1][T2].

## 7) Profit Gate: проверка всех сценариев монетизации
### Сценарий A. Project-only implementation
- Средний проект в РФ-сценарии: 1.8-2.5 млн ₽ выручки, gross margin 35-45% из-за senior delivery и кастомизации [T2].
- Contribution с проекта: ~0.7-1.0 млн ₽ до fixed overhead [T2].
- Чтобы стабильно держать EBITDA >= 500K ₽/мес, нужно закрывать примерно 1 новый проект почти каждый месяц без длинных простоев. Для SAM ~60 млн ₽ и ~24 активных buyer'ов это слишком плотный темп [T1][T2].
- **Вердикт:** FAIL [T2].

### Сценарий B. Managed optimization retainer
- Реалистичный retainer в РФ: 300-450K ₽/мес на клиента, margin после delivery 40-50% [T2].
- Для EBITDA 500K ₽/мес нужно минимум 3-4 активных retainers одновременно, плюс постоянный pipeline replacement [T2].
- При bottom-up SAM ~24 buyer'а и vendor-risk это достижимо только как boutique practice, но не как надёжный investment-grade path [T1][T2].
- **Вердикт:** FAIL [T2].

### Сценарий C. Advisory / training / audit
- Разовые workshops и audit-пакеты можно продавать по 300-600K ₽, но это low-frequency revenue без сильного repeatability [T2][T3].
- Чтобы держать EBITDA 500K ₽/мес, нужен постоянный поток 2-3 продаж ежемесячно, чего не видно в mandatory demand data [T2].
- **Вердикт:** FAIL [T2].

### Итог по Profit Gate
Даже при подтверждённом глобальном WTP локальный РФ market depth недостаточен, чтобы уверенно построить компанию с EBITDA >= 500K ₽/мес на repeatable основе [T1][T2]. **Profit Gate = FAIL.**

## 8) Финальный вывод P4
- **Demand = LOW** [T2].
- **Profit Gate = FAIL** [T1][T2].
- По правилу раннего отклонения кейс должен быть закрыт на стадии demand validation и перемещён в `pipeline/rejected/`.

Sources: T1=4, T2=8, T3=1. Primary evidence basis: T2.