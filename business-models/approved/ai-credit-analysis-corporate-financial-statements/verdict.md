# AI Credit Analysis Corporate Financial Statements
**Статус:** APPROVED
**Итоговый балл:** 77/100
**Дата:** 2026-04-19
**Сектор:** FINTECH

---

## Этап 1 — Описание кейса
Источник сигнала: triage от 2026-04-16 по кейсу Банка «ЦентроКредит» / BPMSoft / DeepSeek. Гипотеза, что AI-анализ отчётности юрлиц уже становится регулярной функцией внутри кредитного контура, а не экспериментальным copilot.

Модель: сервисное внедрение и сопровождение AI-решения для анализа отчётности юридических лиц в кредитных и риск-процессах банков, МФО, лизинговых и факторинговых компаний. Ключевая ценность: сокращение ручного труда кредитных аналитиков, ускорение SLA и стандартизация выводов внутри workflow.

Почему это важно: для enterprise buyer ценность создаёт не просто AI-анализ, а управляемый AI-workflow с интеграцией в CRM/BPM/LOS, журналированием, private contour, SLA и постоянным сопровождением. В таком формате recurring revenue может превышать 500 000 ₽ в месяц.

---

## Этап 2 — Проверка спроса
Итог demand-этапа: **DEMAND = MEDIUM+, LTV Gate = PASS**.

Ключевые сигналы спроса:
- HH.ru: `кредитный аналитик` — **4 888 вакансий**.
- HH.ru: `финансовый анализ отчетности` — **2 019 вакансий**.
- Адресуемая база enterprise buyers: **1 277 организаций** (306 банков, 834 МФО, 100+ лизинговых компаний, 37 факторинговых организаций).

Реальные конкуренты с ценами:
- **Контур.Фокус**: 31 155 ₽, 82 770 ₽, 115 000 ₽.
- **Rusprofile**: 940 ₽/мес, 1 990 ₽/мес.
- **Прима-Информ**: 16 000 ₽/год, 52 000 ₽/год, 65 000 ₽/год, API 975 000 ₽/год.

Telegram/документные AI-сервисы в РФ:
- **OnlyRead**: 35 001 пользователей, тарифы 100 ₽/мес, 950 ₽/мес, 3 490 ₽/мес.
- **БухБот**: тарифы 990 ₽/мес, 1 690 ₽/мес, 3 790 ₽/мес, 6 490 ₽/мес.

TAM / SAM / SOM:
- **TAM:** 3,06 млрд ₽/год.
- **SAM:** 1,764 млрд ₽/год.
- **SOM:** 150 млн ₽/год.

LTV gate по monetization-моделям:
- self-serve SaaS: FAIL;
- usage-based per report: PASS при minimum commit;
- интеграция в CRM/BPM/LOS: PASS;
- managed underwriting workflow: PASS;
- on-prem / private contour / annual license: PASS;
- white-label / embedded: PASS.

Ограничение demand-этапа: mandatory `multi-demand` endpoint не ответил ни на `localhost:9001`, ни на `172.17.0.1:9001`.

---

## Этап 3 — Юнит-экономика
Итог economics-этапа: **PASS**.

Базовые допущения:
- net price: **680 000 ₽/клиент/мес**;
- setup fee: **2,0-3,5 млн ₽**;
- COGS: **235 000 ₽/клиент/мес**;
- contribution: **445 000 ₽/клиент/мес**;
- blended CAC: **1 550 000 ₽**;
- churn benchmark: **1,7%/мес**;
- fixed costs: **4 990 000 ₽/мес**.

Бизнес-процесс:
1. Сбор ICP-аккаунтов.
2. Outbound и выход на risk / credit decision maker.
3. Qualification call.
4. Discovery и demo workflow.
5. Scoping форм отчётности, API и compliance.
6. Pilot proposal и бизнес-кейс.
7. Pilot setup.
8. Валидация коэффициентов и human QA.
9. Security / procurement / legal.
10. Close won и handoff.
11. Production onboarding.
12. Первый invoice и reconciliation оплаты.

Ключевые метрики:
- **LTV (critic model):** ~26,2 млн ₽.
- **LTV/CAC:** 16,9x.
- **CAC Payback:** 3,5 месяца.
- **Contribution Margin:** 65,4%.
- **Break-even:** 12 клиентов, примерно 9-й месяц по operational ramp.

Команда запуска:
Founder, Product Lead, ML/AI Engineer, Backend/Integrations Engineer, Data/Document Engineer, Credit Risk SME, AE, SDR, Implementation Manager, CSM, Finance/Ops/Legal coordinator, 0,5 FTE DevOps/Security. Fixed payroll: **2,93 млн ₽/мес**.

---

## Этап 4 — Финансовая модель и критика
Итог critic-этапа: **CONDITIONAL PASS**.

P&L, базовый сценарий:
- месяц 6: MRR **4,76 млн ₽**, EBITDA **-2,285 млн ₽**;
- месяц 12: MRR **10,2 млн ₽**, EBITDA **675 000 ₽**.

Сценарии:
- оптимистичный месяц 12: MRR **14,28 млн ₽**, EBITDA **2,845 млн ₽**;
- пессимистичный месяц 12: MRR **6,8 млн ₽**, EBITDA **-1,05 млн ₽**.

Структура затрат месяца 12:
- COGS: **3,525 млн ₽**;
- Sales & Marketing: **2,4 млн ₽**;
- R&D: **2,1 млн ₽**;
- G&A: **1,5 млн ₽**;
- EBITDA margin: **6,6%**.

Денежный поток:
- operating EBITDA break-even: **11-й месяц**;
- стартовый капитал до operating BEP: **47,0 млн ₽**;
- peak funding need за год: **49,2 млн ₽**.

Sensitivity:
- **CAC x2:** peak funding need вырастает до ~72,4 млн ₽.
- **Churn x2:** LTV падает до 13,09 млн ₽, month-12 EBITDA почти обнуляется.
- **Price -30%:** month-12 EBITDA уходит в **-2,385 млн ₽**, break-even растёт до **25 клиентов**.

Главные риски:
1. Давление на цену со стороны коробочных data/compliance-игроков.
2. Рост ручного QA и деградация в services business.
3. Длинный enterprise sales cycle и зависание пилотов.
4. Слабая интеграция в workflow, бьющая по продлениям.

Kill conditions:
- к месяцу 6 меньше 5 активных клиентов или pipeline coverage ниже 3x;
- к месяцу 9 COGS > 320 000 ₽/клиент/мес два месяца подряд;
- на трёх подряд новых контрактах net price < 500 000 ₽/мес.

---

## Этап 5 — Финальный вердикт
### Score breakdown
| Критерий | Балл | Максимум |
|---|---:|---:|
| Реальный спрос | 16 | 20 |
| Юнит-экономика | 23 | 25 |
| Масштабируемость | 14 | 20 |
| Конкурентное позиционирование | 9 | 15 |
| Барьеры входа | 7 | 10 |
| Качество данных | 8 | 10 |
| **Итого** | **77** | **100** |

Ключевые метрики для инвесткомитета:
- CAC: **1 550 000 ₽**;
- GM: **65,4%**;
- маржа на клиента: **445 000 ₽/мес**;
- LTV базовый: **8,9 млн ₽**;
- LTV/CAC базовый: **5,7x**;
- CAC payback: **3,5 месяца**;
- break-even: **12 клиентов / 9-й месяц**;
- стартовый капитал: **47,0-49,2 млн ₽**.

Почему approved:
1. Есть подтверждённый buyer budget и платные аналоги в РФ.
2. Экономика проходит фондовый порог с большим запасом.
3. Интеграция в кредитный контур создаёт switching costs и поддерживает high-ACV.

Что доказать до запуска:
1. Два платных пилота с net price не ниже 600 000 ₽/мес.
2. COGS не выше 320 000 ₽/клиент/мес и manual QA ниже 35% кейсов.
3. Хотя бы один on-prem/private contour deployment или formal security approval.

---

## Этап 6 — История прохождения пайплайна
- **Program 4 / Demand Validation:** 16/20, PASS, MEDIUM+ demand.
- **Program 5 / Unit Economics:** PASS, strong enterprise unit economics.
- **Program 6 / Financial Model + Critic:** CONDITIONAL PASS, нужна дисциплина по цене, QA и GTM.
- **Program 7 / Critic and Verdict:** APPROVED, **77/100**.
