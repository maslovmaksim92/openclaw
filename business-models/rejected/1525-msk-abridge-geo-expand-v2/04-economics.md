---
stage: economics
case: 1525-msk-abridge-geo-expand-v2
date: 2026-04-20
analyst: branch-models-lead
verdict: PASS_WITH_CONSTRAINTS
confidence: medium
investment_grade: false
sector: GEO-EXPAND
---

# 04-economics — Unit Economics

## Кейс
Abridge GEO Expand v2, ambient clinical documentation для крупных клиник и health systems с локализацией под РФ.

## Executive summary

**Итог P5: PASS WITH CONSTRAINTS.**

Экономика проходит только в enterprise / network-on-prem сценарии. Если продавать продукт как «диктовку для одного врача», модель ломается. Если продавать как контур `speech-to-note + structured protocols + QA documentation + интеграции с МИС`, путь к `EBITDA > 500 тыс. ₽/мес` появляется.

Ключевые выводы:
1. **Self-serve сценарий невалиден**: низкий search-demand, высокие требования к локализации и длинный цикл доверия в медицине убивают дешёвую модель.
2. **Mid-market / enterprise сценарий реалистичен**: контракт **220–380 тыс. ₽/мес** на клинику или контур врачей уже даёт рабочую contribution economics.
3. **Главный риск в service-load**: интеграции с МИС, обучение врачей, QA и compliance быстро съедают маржу.
4. **Investment grade пока нет**: кейс выглядит экономически допустимым, но запас прочности средний, а GTM execution-heavy.

## 1. Модель и ключевые допущения

### ICP
- крупные частные сети клиник;
- цифрово зрелые многопрофильные медцентры;
- группы клиник, где ценится скорость врача, качество документации и управляемость протоколов;
- контуры, готовые к on-prem или закрытому облаку из-за медданных.

### Base-case для РФ
- Средний recurring контракт: **280 000 ₽/клиент/мес**
- Setup / onboarding / integration fee: **500 000 ₽** разово
- Для основной математики считаю recurring отдельно, setup fee не включаю в MRR.
- Средний rollout: **20-50 врачей** на один активный аккаунт.

### Почему беру 280k ₽ MRR
Это выше low-end speech tools и ниже тяжёлого hospital-grade enterprise deal. Такой чек выглядит правдоподобным для РФ, если продавать не только транскрипт, а экономию времени врача, протоколирование, контроль качества и интеграцию с МИС.

## 2. Business process table: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | ICP mapping по сетям клиник | SDR / founder | CRM, Rusprofile, manual research | 2 ч | 2 000 | Низкий |
| 2 | Первичный outreach | SDR | Email, Telegram, phone | 1.5 ч | 1 600 | Средний |
| 3 | Qualification call | SDR + AE | Meet, CRM | 1 ч | 3 000 | Средний |
| 4 | Discovery по документообороту врача | AE + founder | Meet, questionnaire | 2 ч | 8 500 | Низкий |
| 5 | Demo на реальных сценариях приёма | AE + clinical specialist | Demo env, scripts | 2 ч | 9 500 | Низкий |
| 6 | Security / legal / data residency pre-check | AE + CTO | NDA, policy docs | 2 ч | 8 500 | Низкий |
| 7 | Pilot scoping и ROI-гипотеза | AE + CSM | SOW, ROI sheet | 3 ч | 12 000 | Низкий |
| 8 | Интеграция с МИС / шаблонами / ролями | Solutions + CSM | API, mappings, templates | 18 ч | 58 000 | Средний |
| 9 | Обучение врачей и админов | CSM | Zoom, manuals | 5 ч | 14 000 | Средний |
| 10 | Пилот 4-6 недель и weekly review | CSM + AE | Analytics, support | 12 ч | 34 000 | Средний |
| 11 | Procurement / договор / счёт | AE + founder + ops | Contract workflow | 6 ч | 16 000 | Низкий |
| 12 | Production rollout после оплаты | CSM + support | Runbook, dashboards | 8 ч | 22 000 | Средний |

### Вывод по процессу
Продажа выглядит как **consultative healthcare B2B sale**. До оплаты много ручного труда и trust-building, поэтому низкий CAC здесь был бы неправдоподобен.

## 3. COGS per client / month

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| Speech / LLM / inference budget | 30 000 | регулярные note-generation и summaries |
| Hosting / storage / logs | 16 000 | закрытый контур, хранение, audit trail |
| Support L1-L2 | 18 000 | доля support-инженера |
| CSM / account ops | 24 000 | доля CSM на активный аккаунт |
| Clinical QA / templates | 18 000 | шаблоны и выборочная проверка |
| Integration amortization | 22 000 | spread setup effort over 12 мес |
| Security / compliance allocation | 12 000 | legal и процессный overhead |
| **Итого COGS** | **140 000** |  |

### Выручка и валовая маржа
- MRR на клиента: **280 000 ₽**
- COGS на клиента: **140 000 ₽**
- Gross profit на клиента: **140 000 ₽**
- **Gross Margin = 50.0%**

### Комментарий
Для медтеха с интеграциями и требованиями к данным валовая маржа на уровне **50%** выглядит реалистично, но только если внедрение постепенно стандартизируется.

## 4. CAC by channel + funnel conversion

### Воронка по каналам

| Канал | Leads/мес | MQL | SQL | Pilot | New paying customers | Lead→Paying |
|---|---:|---:|---:|---:|---:|---:|
| Founder-led / network | 18 | 7 | 4 | 2 | 0.8 | 4.4% |
| Targeted outbound по клиникам | 110 | 16 | 7 | 3 | 0.7 | 0.64% |
| Content / inbound / events | 35 | 8 | 4 | 2 | 0.4 | 1.1% |
| Partnerships / МИС / integrators | 10 | 4 | 2 | 1 | 0.3 | 3.0% |
| **Итого blended** | **173** | **35** | **17** | **8** | **2.2** | **1.27%** |

### Fully-loaded CAC

| Компонент | ₽/мес | Как получено |
|---|---:|---|
| Paid acquisition / category tests | 160 000 | ограниченные B2B healthcare кампании |
| SDR + AE FOT attributed to new | 980 000 | 2 SDR + 1 AE + взносы + commissions |
| Marketing allocation | 220 000 | контент, кейсы, вебинары |
| CRM / sequencing / tooling | 90 000 | CRM, телефония, enrichment |
| Events / partnerships | 170 000 | отраслевые мероприятия и партнёры |
| Overhead multiplier (x1.3) | 486 000 | admin / management / ops overhead |
| **Итого fully-loaded acquisition spend** | **2 106 000** |  |

- New paying customers / мес: **2.2**
- **Blended fully-loaded CAC = 957 273 ₽**

### Sanity check
Для regulated B2B healthtech CAC около **0.95 млн ₽** выглядит жёстко, но правдоподобно. Ниже **300 тыс. ₽** для такого motion было бы явным занижением.

## 5. LTV и churn

### Базовые допущения
- MRR на клиента: **280 000 ₽**
- ARR на клиента: **3 360 000 ₽**
- Gross Margin: **50%**
- Annual logo churn: **20%**

Формула:

`LTV = ARR × GM / churn`

`LTV = 3 360 000 × 50% / 20% = 8 400 000 ₽`

### Вывод
- **LTV = 8.4 млн ₽**
- Значение рабочее, но сильно зависит от реального renewal после пилота и от того, насколько клиники не откатываются на старые workflow.

## 6. LTV / CAC

- LTV: **8 400 000 ₽**
- Fully-loaded CAC: **957 273 ₽**

`LTV/CAC = 8 400 000 / 957 273 = 8.8x`

### Stress-case
Чтобы не переоценить кейс, считаю также stress-case:
- Effective GM в Year 1: **42%**
- Annual churn: **30%**

`Stress LTV = 3 360 000 × 42% / 30% = 4 704 000 ₽`

`Stress LTV/CAC = 4 704 000 / 957 273 = 4.9x`

### Вердикт по метрике
Даже в stress-case LTV/CAC остаётся выше порога **3:1**. Значит, проблема кейса не в формальном LTV/CAC, а в burn и длинном цикле внедрения.

## 7. CAC Payback

`CAC Payback = CAC / MRR per customer`

`957 273 / 280 000 = 3.4 мес`

Если считать payback по gross profit:

`957 273 / 140 000 = 6.8 мес`

### Комментарий
Gross-profit payback **6.8 мес** выглядит допустимо для healthcare B2B. Но это требует дисциплины по integration scope, иначе COGS быстро поползёт вверх.

## 8. Contribution Margin %

Для contribution margin беру выручку минус COGS минус variable success / commission load.

- Revenue per client / мес: **280 000 ₽**
- COGS: **140 000 ₽**
- Variable commission + success allocation: **18 000 ₽**

`Contribution profit = 122 000 ₽`

`Contribution Margin = 122 000 / 280 000 = 43.6%`

### Вывод
**Contribution Margin = 43.6%**. Это здоровый, но не защищённый показатель. Если кейс станет слишком кастомным, запас быстро исчезнет.

## 9. Team & FOT

| Роль | Нужно чел. | Salary gross ₽/мес | Time-to-hire (мес) | Ramp (мес) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO / founder | 1 | 550 000 | 0 | 0 | 165 000 | 715 000 |
| CTO / tech lead | 1 | 520 000 | 2 | 2 | 156 000 | 676 000 |
| Backend engineer | 2 | 380 000 | 1.5 | 1.5 | 114 000 | 988 000 |
| ML / applied AI engineer | 1 | 480 000 | 2 | 2 | 144 000 | 624 000 |
| Integrations / solutions engineer | 1 | 330 000 | 1.5 | 1.5 | 99 000 | 429 000 |
| SDR | 2 | 150 000 + бонус | 1 | 1 | 45 000 | 390 000 |
| AE | 1 | 280 000 + комиссия | 1.5 | 2 | 84 000 | 364 000 |
| CSM / implementation | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Clinical SME / QA | 1 | 280 000 | 1.5 | 1.5 | 84 000 | 364 000 |
| Finance / ops (part-time) | 0.5 | 120 000 | 1 | 0.5 | 36 000 | 156 000 |
| **Итого full team FOT** | **11.5** |  |  |  |  | **4 992 000 ₽/мес** |

## 10. Fixed costs breakdown

| Статья | ₽/мес |
|---|---:|
| Full team FOT | 4 992 000 |
| Cloud base platform not in COGS | 300 000 |
| Security / legal / meddata compliance | 240 000 |
| G&A / бухгалтерия / ЭДО / misc | 100 000 |
| Travel / enterprise meetings | 90 000 |
| Office / admin | 120 000 |
| **Итого fixed costs** | **5 842 000 ₽/мес** |

## 11. Break-even

### Break-even by client count
- Contribution profit per client / мес: **122 000 ₽**
- Fixed costs: **5 842 000 ₽/мес**

`Break-even clients = 5 842 000 / 122 000 = 47.9`

### Founder-mode / lean team
Если первые 12-15 месяцев держать компактную команду и fixed costs на уровне **3 550 000 ₽/мес**, тогда:

`3 550 000 / 122 000 = 29.1 клиентов`

### Вывод
- На **полной команде** break-even тяжёлый, почти **48 клиентов**.
- В **lean founder-mode** модель становится рабочей около **29-30 клиентов**.
- Следовательно, кейс проходит только при очень осторожном найме и productized delivery.

## 12. Burn-to-breakeven и runway

### Burn base-case
- Fixed costs lean-mode: **3.55 млн ₽/мес**
- Acquisition spend: **2.11 млн ₽/мес**
- Total early burn: **~5.66 млн ₽/мес**

### Burn-to-breakeven
Если компания растёт до **30 клиентов** за **18-24 месяца**, ориентир burn-to-breakeven будет **58-78 млн ₽** в зависимости от темпа пилотов и реальной скорости интеграций.

### Runway
При `startup_capital = 80 млн ₽`:

`80 000 000 / 5 660 000 ≈ 14.1 мес`

С учётом нарастающей выручки реалистичный runway: **15-17 месяцев**.

## 13. Что происходит при 40 клиентах

### P&L snapshot при 40 клиентах
- Revenue: `40 × 280 000 = 11 200 000 ₽/мес`
- COGS: `40 × 140 000 = 5 600 000 ₽/мес`
- Gross profit: **5 600 000 ₽/мес**
- Variable commission / success: `40 × 18 000 = 720 000 ₽/мес`
- Contribution profit: **4 880 000 ₽/мес**

Если fixed costs держатся в lean-mode **3.55 млн ₽**, тогда:
- **EBITDA ≈ 1.33 млн ₽/мес**

Если команда раздута до steady-state **5.84 млн ₽**, тогда:
- **EBITDA ≈ -0.96 млн ₽/мес**

### Ключевой вывод
Profit gate проходит **только при дисциплинированной операционной модели**. Ранний heavy hiring ломает экономику даже при хорошем ARR.

## 14. Profit Gate

### Проверка правила
Условие FAIL: `company EBITDA < 500K/mo achievable even at 50 clients` или `LTV/CAC < 1:1`

### Факт
- LTV/CAC уверенно выше **1:1** и выше инвестиционного порога.
- EBITDA **> 500 тыс. ₽/мес достижима** в lean-mode уже около **34-36 клиентов**.
- На тяжёлой команде кейс быстро становится пограничным.

## Итоговый вердикт P5

**PASS WITH CONSTRAINTS.**

Кейс экономически допустим только как enterprise healthcare operator с закрытым контуром, интеграциями и контролем документооборота. Как дешёвый AI-scribe для одиночных врачей модель в РФ не выглядит жизнеспособной.

## Что нужно проверить на следующем этапе
1. Насколько реалистично удержать чек **280 тыс. ₽+/мес** в российских private healthcare сетях.
2. Не окажется ли фактический churn выше **25-30%** из-за длинного внедрения и слабого adoption врачами.
3. Можно ли реально productize integrations и clinical QA, иначе contribution margin быстро деградирует.

## Источники
- `pipeline/cases/1525-msk-abridge-geo-expand-v2/02-demand.md`
- Публичные ценовые и рыночные якоря, уже собранные в `02-demand.md`
- Консервативная внутренняя модель branch-models-lead для regulated B2B healthtech / GEO-EXPAND кейсов
