# AI-урегулирование убытков и антифрод для страховщиков

[FINTECH] AI-урегулирование убытков и антифрод для страховщиков — APPROVED WITH NOTES: 71/100 | EBITDA base=1161К₽/мес через 15 мес | LTV/CAC=18,6x | Ключевое преимущество: регуляторно ускоренный claims workflow для страховщиков | Главный риск: длинный enterprise sales cycle и price compression.

- slug: `ai-uregulirovanie-ubytkov-i-antifrod-dlya-strahovshchikov`
- sector: `FINTECH`
- status: `APPROVED WITH NOTES`
- score: `71/100`
- date: `2026-04-25`

## Стадия 1. Intake
- Wedge: AI-сервис для страховщиков автоматически принимает и классифицирует заявления на урегулирование убытков, проверяет признаки мошенничества по фото и документам и отправляет простые кейсы на выплату без участия урегулировщика.
- Why now: с 1 января 2025 года электронное урегулирование убытков по ОСАГО стало обязательным, а поток дистанционных заявлений уже измеряется сотнями тысяч.
- Начальная гипотеза EBITDA: 0,9-3,0 млн ₽/мес в горизонте 24 месяцев.

## Стадия 2. Validation
- В папке кейса отдельный файл `02-validation.md` отсутствует.
- Validation-логика фактически встроена в `02-demand.md` и последующие финансовые стадии.
- Это process-gap, но не блокер для финального verdict, потому что ключевые demand и economics evidence присутствуют.

## Стадия 3. Demand
- Exact-demand по category label слабый: Demand API вернул LOW.
- При этом underlying budget line доказана: страховые премии в РФ 3,7 трлн ₽, 129 страховщиков, SAM по кейсу 1,44-2,00 млрд ₽.
- Публичные price anchors SEON, ComplyAdvantage, Featurespace и JuicyScore подтверждают willingness to pay за fraud/risk automation.
- Source tier balance: T1=9, T2=6, T3=0, weighted=2,60.

## Стадия 4. Economics
- customer_ltv_rub: 54 666 667 ₽
- CAC fully-loaded: 2 942 000 ₽
- LTV/CAC: 18,6x
- CAC payback: 2,45 мес
- GM: 68,3%
- contribution_margin_rub_month: 820 000 ₽ на клиента
- break-even: 11 клиентов
- clients_to_500k_ebitda: 12
- months_to_500k_ebitda: 15
- startup_capital_to_bep_rub: 65 966 000 ₽
- рекомендованный стартовый капитал с буфером: 90 000 000 ₽

## Стадия 5. Critic
- Base-case проходит EBITDA gate, но Monte Carlo downside тяжёлый: p10 EBITDA @M24 = -5,45 млн ₽/мес.
- Главные риски: founder dependency в enterprise sales, price compression на тендерах, vendor/LLM/GPU dependency.
- Конкурентная карта подтверждает окно для локального insurer-stack в РФ-контуре, но moat пока только умеренный.

## Стадия 6. Verdict
### Scorecard
| # | Критерий | Raw |
|---|---|---:|
| 1 | Unit Economics | 20 |
| 2 | EBITDA Potential | 19 |
| 3 | Market + Demand | 18 |
| 4 | Moat | 15 |
| 5 | Execution Risk | 15 |
| 6 | GTM Realism | 19 |

**Итого raw:** 106/150  
**Normalized:** 71/100

### Почему одобрено
1. Очень сильная unit economics при regulated enterprise pricing.
2. EBITDA > 500 тыс. ₽/мес достигается за 15 месяцев при 12 клиентах.
3. Есть регуляторный tailwind и измеримый ROI через antifraud и cost-to-serve.

### Почему только with notes
1. Category demand остаётся education-heavy.
2. Moat ещё не доказан на уровне proprietary data/distribution.
3. Downside чувствителен к pricing и скорости продаж.

### 10 named targets
СОГАЗ, АльфаСтрахование, Ингосстрах, РЕСО-Гарантия, Росгосстрах, СберСтрахование, ВСК, Ренессанс Страхование, Югория, Абсолют Страхование.

### Investment committee next step
Финансировать только milestone-based tranche после подтверждения 2 paid insurers, partner channel и контролируемой средней скидки не выше 20%.

## Артефакты
- `pipeline/approved/ai-uregulirovanie-ubytkov-i-antifrod-dlya-strahovshchikov/01-intake.md`
- `pipeline/approved/ai-uregulirovanie-ubytkov-i-antifrod-dlya-strahovshchikov/02-demand.md`
- `pipeline/approved/ai-uregulirovanie-ubytkov-i-antifrod-dlya-strahovshchikov/04-economics.md`
- `pipeline/approved/ai-uregulirovanie-ubytkov-i-antifrod-dlya-strahovshchikov/05-critic.md`
- `pipeline/approved/ai-uregulirovanie-ubytkov-i-antifrod-dlya-strahovshchikov/06-verdict.md`
