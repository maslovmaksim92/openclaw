---
stage: economics
case: 0806-msk-securitypal-refresh-geo-expand-v2
date: 2026-04-20
analyst: branch-models-lead
verdict: FAIL
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
SecurityPal-подобный AI-native customer assurance слой для security questionnaires, trust center и vendor security review у B2B software и enterprise-tech компаний.

## Executive summary

### Итоговый вывод
**Экономика неинвестиционная.**

Причины:
1. **Fully-loaded CAC = 3 853 143 ₽ на нового платящего клиента**, что для локального enterprise trust-workflow wedge слишком тяжело.
2. **LTV = 2 964 286 ₽**, **LTV/CAC = 0,77x**, то есть ниже даже fail-порога **1:1**.
3. **CAC Payback = 21,4 месяца**, что хуже базового порога <12 мес и хуже enterprise-порога <18 мес.
4. При реалистичной service-heavy delivery-модели **EBITDA остаётся отрицательной даже на 50 клиентах**.

### Ключевые рабочие допущения
- Реалистичный локальный MRR на 1 клиента: **180 000 ₽/мес**.
- Разовый setup/pilot: **450 000 ₽**, но для payback считаю только recurring MRR.
- COGS на клиента: **97 000 ₽/мес**.
- Gross Margin: **46,1%**.
- Contribution Margin после переменных sales/serving затрат: **35,6%**.
- Logo churn: **2,8% в месяц**.

## 1. Бизнес-процесс от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | ICP-список и приоритизация аккаунтов | Founder + SDR | HH/LinkedIn analogs, таблица ICP, CRM | 1 день | 8 000 | Low |
| 2 | Enrichment контактов и сегментация | SDR | CRM, email finder, ручной ресерч | 0,5 дня | 5 000 | Medium |
| 3 | Первый outbound-touch | SDR | Email sequencer, LinkedIn, Telegram/email | 7-10 дней | 18 000 | Medium |
| 4 | Ответы и назначение discovery | SDR | CRM, календарь, почта | 3 дня | 9 000 | Medium |
| 5 | Discovery call и pain qualification | AE + founder | Zoom/Meet, CRM | 1 неделя | 22 000 | Low |
| 6 | Demo trust-center + questionnaire workflow | AE + Product/GRC | Demo env, презентация, knowledge base | 1 неделя | 27 000 | Low |
| 7 | Pilot scoping и security/GRC audit | AE + GRC lead | Notion/Docs, шаблоны questionnaire mapping | 1-2 недели | 54 000 | Low |
| 8 | Pilot delivery, первые ответы на анкеты | Analyst + AI platform | LLM stack, KB, workflow platform | 2-4 недели | 96 000 | Medium |
| 9 | Procurement, legal, DPA, infosec review | Founder + AE + legal external | Договоры, ЭДО, security docs | 3-6 недель | 61 000 | Low |
| 10 | Onboarding и интеграция с trust center | CSM + DevOps | Cloud, SSO, KB import | 1-2 недели | 43 000 | Medium |
| 11 | Первый monthly service cycle | CSM + analyst pool | Dashboard, task tracker, AI copilots | 1 месяц | 97 000 | Medium |
| 12 | Invoice, акт, оплата | Finance/ops | Банк, ЭДО, CRM billing | 5-10 дней | 6 000 | High |

### Вывод по процессу
Сделка длинная и многокасательная. Ключевой bottleneck, это не генерация лидов, а **pilot + procurement + infosec review**, поэтому кейс по факту ближе к enterprise services-led SaaS, чем к чистому software-self-serve.

## 2. Pricing и revenue model

| Компонент | Значение |
|---|---:|
| Разовый pilot/setup | 450 000 ₽ |
| Ежемесячный recurring fee | 180 000 ₽ |
| Средний contract length в модели | 36 месяцев max, но считаю через churn |
| Расчётный ARPA / MRR per client | 180 000 ₽/мес |

### Почему беру 180 000 ₽, а не 250 000 ₽
В 02-demand был midpoint 250 000 ₽/мес, но для РФ-модели это слишком оптимистично, потому что:
- у категории есть **free-entry trust center**;
- сильный overlap с Conveyor/SafeBase-like trust workflow;
- часть value сидит в human concierge и сложнее защищается pricing power;
- локальный buyer часто начинает с пилота и скидки, а не с full enterprise package.

## 3. COGS breakdown на клиента в месяц

| Статья COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| GRC/security analyst delivery | 45 000 | ~0,16 FTE analyst на клиента при fully-loaded cost ~286k ₽/мес |
| CSM / service coordination | 12 000 | ~0,04 FTE Customer Success при fully-loaded cost ~312k ₽/мес |
| LLM/API inference и AI workflow | 8 000 | inference + reruns + embedding + guardrails |
| Cloud / storage / audit logs | 6 000 | hosting, encrypted storage, backups |
| Security/compliance tooling | 5 000 | scanner, knowledge base, doc processing |
| QA / rework / escalation reserve | 10 000 | human correction на сложных анкетах |
| On-call presales support amortized | 7 000 | повторные уточнения и ответы после go-live |
| Vendor management / misc | 4 000 | внешние подписки и документы |
| **Итого COGS** | **97 000** |  |

### Gross Margin
- Revenue per client: **180 000 ₽/мес**
- COGS per client: **97 000 ₽/мес**
- **Gross Profit per client = 83 000 ₽/мес**
- **Gross Margin = 46,1%**

### Комментарий
Для software-only SaaS это слабая маржа. Для managed security-response слоя она реалистична, но именно она убивает scale economics.

## 4. CAC по каналам с funnel conversion

### Channel CAC
| Канал | Monthly spend, ₽ | Воронка | New paying customers / мес | Raw CAC, ₽ |
|---|---:|---|---:|---:|
| Founder-led outbound / ABM | 790 000 | 300 target accounts → 36 replies (12%) → 15 meetings (41,7%) → 6 SQL (40%) → 2 pilots (33,3%) → 0,45 win (22,5%) | 0,45 | 1 755 556 |
| Content / webinars / thought leadership | 186 000 | 140 MQL → 14 demo (10%) → 4 SQL (28,6%) → 1 pilot (25%) → 0,15 win (15%) | 0,15 | 1 240 000 |
| Partners / referrals / VC-network intros | 250 000 | 12 intros → 6 meetings (50%) → 3 SQL (50%) → 1 pilot (33,3%) → 0,10 win (10%) | 0,10 | 2 500 000 |
| **Blended raw** | **1 226 000** | blended | **0,70** | **1 751 429** |

### Вывод по каналам
- Самый рабочий канал, это founder-led outbound, но он плохо масштабируется.
- Content дешевле, но даёт мало win-rate в узкой security trust category.
- Partners выглядят красиво на входе, но цикл медленный и win-rate низкий.

## 5. FULLY-LOADED CAC

### Формула
**Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing team FOT allocated + Tools/CRM + Events + Multiplier overhead) / New paying customers**

### Таблица компонентов
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK / niche media tests) | 80 000 | тестовый performance budget для retargeting + branded demand capture | assumption, conservative test budget |
| Outbound team FOT (SDR/AE attributed to new) | 769 000 | SDR fully-loaded 224k + 80% AE fully-loaded 334k + 25% founder-sales allocation 211k | HH.ru salary benchmark + 30% соцвзносы |
| Marketing team FOT (partial allocation) | 182 000 | 0,5 Product/GRC lead allocation 208k + 0,3 founder allocation 126k, минус overlap округлён | HH.ru benchmark / founder allocation |
| Tools (CRM, sequencing, data, webinar stack) | 95 000 | CRM + outbound stack + webinar + docs + enrichment | SaaS stack assumption |
| Events / partnerships | 100 000 | 1 нишевое событие / партнерские активности в среднем по месяцу | assumption |
| Raw acquisition spend subtotal | 1 226 000 | сумма выше | calculated |
| Overhead multiplier (x2,2 для enterprise motion) | 1 471 200 | raw CAC × (2,2 - 1,0), учтены RFP, security review, procurement, management overhead | pipeline methodology for enterprise >500k ACV equivalent complexity |
| **Fully-loaded acquisition spend** | **2 697 200** | raw subtotal + overhead | calculated |

### Fully-loaded CAC result
- New paying customers / month: **0,70**
- **Fully-loaded CAC = 2 697 200 / 0,70 = 3 853 143 ₽**

### Sanity checks
1. **CAC Payback = CAC / MRR = 3 853 143 / 180 000 = 21,4 месяца**
2. **LTV/CAC = 0,77x**
3. CAC не ниже benchmark, а наоборот намного выше, что указывает на слабую scale-эффективность категории в локальном запуске.
4. Channel CAC и blended CAC показаны отдельно.

## 6. LTV и churn

### Benchmark source
По ChartMogul для SaaS monthly customer churn сильно зависит от ARPA: у high-ARPA B2B он обычно ниже consumer/SMB, но верхняя часть распределения всё равно уходит в район 2%+ monthly churn. Для данного кейса беру **2,8% monthly logo churn**, то есть хуже хорошего enterprise SaaS benchmark, потому что:
- продукт не system-of-record;
- часть value коммодитизируется free trust center;
- есть риск downgrade в более дешёвый workflow;
- high-touch service layer делает renewals чувствительными к качеству delivery.

### Расчёт LTV
- ARPA: **180 000 ₽/мес**
- Gross Profit per client: **83 000 ₽/мес**
- Churn rate: **2,8% / мес**
- **LTV = 83 000 / 0,028 = 2 964 286 ₽**

## 7. LTV/CAC ratio

| Метрика | Значение |
|---|---:|
| LTV | 2 964 286 ₽ |
| Fully-loaded CAC | 3 853 143 ₽ |
| **LTV/CAC** | **0,77x** |

### Вывод
Для investment-grade нужен минимум **3,0x**. Здесь показатель **ниже 1,0x**, значит на каждый новый рубль валовой прибыли компания тратит больше, чем потом возвращает на жизненном цикле клиента.

## 8. CAC Payback

| Метрика | Значение |
|---|---:|
| Fully-loaded CAC | 3 853 143 ₽ |
| MRR per customer | 180 000 ₽ |
| **CAC Payback** | **21,4 месяца** |

### Вывод
Даже по enterprise-допуску <18 месяцев кейс не проходит.

## 9. Contribution Margin

### Переменные затраты сверх COGS на клиента в месяц
| Статья | ₽/клиент/мес |
|---|---:|
| Sales commission / variable bonus | 12 000 |
| Payment / docs / billing ops | 2 000 |
| Travel / customer workshop reserve | 5 000 |
| **Итого variable non-COGS** | **19 000** |

### Расчёт
- Revenue: **180 000 ₽**
- Minus COGS: **97 000 ₽**
- Minus variable non-COGS: **19 000 ₽**
- Contribution profit: **64 000 ₽**
- **Contribution Margin = 35,6%**

## 10. Team & FOT

### Полная команда
| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder-sales | GTM, fundraising, complex deals | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | архитектура, security platform, integrations | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | workflow engine, KB, APIs | 420 000 | 126 000 | 546 000 |
| Senior Backend #2 | questionnaire pipeline, integrations | 420 000 | 126 000 | 546 000 |
| ML Engineer | AI-answering, retrieval, evaluation | 500 000 | 150 000 | 650 000 |
| DevOps / Security infra | hosting, observability, IAM | 350 000 | 105 000 | 455 000 |
| Product / GRC Lead | domain templates, compliance logic, demos | 320 000 | 96 000 | 416 000 |
| SDR | outbound prospecting | 172 500 | 51 750 | 224 250 |
| AE | demos, pilots, close | 321 000 | 96 300 | 417 300 |
| Customer Success | onboarding, renewals, support | 240 000 | 72 000 | 312 000 |
| Security Analyst | human-in-the-loop delivery | 220 000 | 66 000 | 286 000 |
| **Итого** |  |  |  | **5 412 550 ₽/мес** |

### Таблица найма, time-to-hire и ramp
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2,5 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1,5 | 1,5 | 126 000 | 546 000 each |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 0 | 0 | - | - | - | 0 |
| SDR (outbound) | 1 | 172 500 | 1 | 1 | 51 750 | 224 250 |
| AE (Account Exec) | 1 | 321 000 | 1,5 | 2,5 | 96 300 | 417 300 |
| Customer Success | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |
| Customer / Security Analyst | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |

### Hiring realism комментарий
- В M1 нет unrealistic найма 5+ человек.
- Основная узкая шейка, это **CTO/ML/GRC hiring**.
- До выхода команды на рабочую форму проходит 4-6 месяцев, поэтому GTM до этого времени founder-heavy и дорогой.

## 11. Cumulative FOT timeline M1-M12

| Месяц | Кто подключён | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO + внешние подрядчики/контур MVP | 1 095 000 |
| M2 | + Product/GRC Lead | 1 511 000 |
| M3 | + CTO/Tech Lead + SDR | 2 450 250 |
| M4 | + Backend #1 + AE | 3 413 550 |
| M5 | + DevOps + Customer Success | 4 180 550 |
| M6 | + ML Engineer | 4 830 550 |
| M7 | + Security Analyst | 5 116 550 |
| M8 | + Backend #2 | 5 662 550 |
| M9 | стабилизация команды | 5 662 550 |
| M10 | стабилизация команды | 5 662 550 |
| M11 | стабилизация команды | 5 662 550 |
| M12 | стабилизация команды | 5 662 550 |

### Вывод по FOT timeline
Даже аккуратный hire-plan даёт выход на **5,66 млн ₽/мес** FOT к M8. Для узкого trust-workflow wedge это слишком тяжёлый fixed-cost base.

## 12. Fixed costs breakdown

| Статья fixed costs | ₽/мес |
|---|---:|
| Core team FOT, не сидящий в COGS | 4 012 550 |
| Office / legal / бухгалтерия / admin | 180 000 |
| Core cloud/platform minimum | 220 000 |
| Security/compliance baseline | 130 000 |
| Product/design/misc contractors | 180 000 |
| G&A reserve | 167 450 |
| **Итого fixed costs** | **4 890 000 ₽/мес** |

## 13. Break-even

### По количеству клиентов
- Contribution profit на клиента: **64 000 ₽/мес**
- Fixed costs: **4 890 000 ₽/мес**
- **Break-even = 4 890 000 / 64 000 = 76,4 клиента**
- Округлённо: **77 клиентов**

### По месяцам
При текущем blended GTM темпе **0,7 нового платящего клиента в месяц** break-even наступил бы примерно через **110 месяцев**, что неприемлемо.

Даже если после разгона предположить **4 новых клиента в месяц**, break-even по клиентской базе наступает только около **M20**, то есть **не достигается в M1-M12**.

### Проверка 50 клиентов
- Revenue: **9 000 000 ₽/мес**
- Contribution profit: **50 × 64 000 = 3 200 000 ₽/мес**
- EBITDA: **3 200 000 - 4 890 000 = -1 690 000 ₽/мес**

**Даже на 50 клиентах EBITDA остаётся отрицательной.**

## 14. Burn-to-breakeven

Даже при ускоренном найме и вменяемом GTM экономика выглядит так:
- burn на ранней фазе M1-M4: **2,5-3,8 млн ₽/мес**;
- burn на рабочей фазе M6-M12: **4,5-5,3 млн ₽/мес** после выручки первых клиентов;
- капитал до реалистичного break-even: **не менее 60-70 млн ₽**, если считать 18-20 месяцев, длинный enterprise cycle и service-heavy delivery.

### Вывод
Для fund-level standalone кейса это слишком тяжёлая capital requirement при слабой unit economics.

## 15. Cash runway

### Допущение
- startup_capital = **35 000 000 ₽**
- средний net burn в модели = **4 100 000 ₽/мес**

### Расчёт
- **Cash runway = 35 000 000 / 4 100 000 = 8,5 месяца**

### Вывод
Для enterprise B2B SaaS с длинным циклом продажи runway меньше 9 месяцев, это red flag.

## 16. Итоговый verdict по economics

### Что проходит
- Рынок и pain существуют.
- Можно продавать pilot/setup.
- Есть понятный enterprise workflow и глобальные category anchors.

### Что не проходит
1. **LTV/CAC = 0,77x** < **1,0x fail gate**.
2. **CAC Payback = 21,4 мес** > допустимого.
3. **Contribution Margin = 35,6%** слишком низкая для тяжёлого enterprise CAC.
4. **Break-even = 77 клиентов**, а при **50 клиентах EBITDA всё ещё отрицательная**.
5. Модель требует много капитала до масштаба, но не даёт достаточной защиты unit economics.

## Источники
- 02-demand кейса: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/0806-msk-securitypal-refresh-geo-expand-v2/02-demand.md
- SecurityPal Questionnaire Concierge: https://www.securitypalhq.com/products/security-questionnaire-concierge
- SecurityPal Trust Center: https://www.securitypalhq.com/products/trust-center
- Conveyor pricing: https://www.conveyor.com/pricing
- SafeBase pricing: https://safebase.io/pricing
- Loopio pricing: https://loopio.com/pricing/
- ChartMogul churn benchmarks: https://chartmogul.com/saas-metrics/customer-churn/
- HH.ru, backend engineer salaries: https://hh.ru/search/vacancy?text=Senior+Backend+%D1%80%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%87%D0%B8%D0%BA&area=1
- HH.ru, DevOps salaries: https://hh.ru/search/vacancy?text=DevOps&area=1
- HH.ru, ML engineer salaries: https://hh.ru/search/vacancy?text=ML+Engineer&area=1
- HH.ru, SDR salaries: https://hh.ru/search/vacancy?text=SDR&area=1
- HH.ru, Account Executive salaries: https://hh.ru/search/vacancy?text=Account+Executive&area=1
- HH.ru, Product Manager salaries: https://hh.ru/search/vacancy?text=Product+Manager&area=1
