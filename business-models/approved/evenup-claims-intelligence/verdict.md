# evenup-claims-intelligence

## Stage 0. Brief

### Исходный тезис
EvenUp, вертикальная AI-платформа для plaintiff-side personal injury law, показывает, что claims-intelligence категория уже масштабируется на зрелом рынке. Для РФ гипотеза в том, что похожий workflow можно локализовать под автоюристов, страховые споры, вред здоровью и массовые consumer claims.

### Почему кейс был создан
- категория узкая, не шумовая;
- есть сильный внешний proof через EvenUp;
- потенциальный продукт встраивается в ежедневный workflow, а не остаётся feature-layer.

### Источники brief
- `00-brief.md`
- https://www.evenuplaw.com/blog/evenup-2b-valuation/
- https://www.forbes.com/companies/evenup/
- https://companies.rbc.ru/news/EasrSbMloN/chto-proishodit-v-legaltech-kak-ii-menyaet-rabotu-yuristov-v-rossii/
- https://ailawyer.ru/

---

## Stage 1. Demand

### Verdict
**PASS**

### Demand summary
- Composite demand: **MEDIUM**
- GEO-EXPAND: **YES**
- LTV gate: **PASS**, но только для enterprise ICP

### Что подтверждает спрос
- EvenUp: **2000+ firms**, **200 000+ cases**, **$10B+ damages**, **10 000 cases weekly**
- pricing anchors:
  - DemandCraft: **$99 / $249 / $599 в месяц**
  - CaseMark: **$25 / $50 за summary**, **$5/час transcription**
  - Paxton: **$499/user/month**
- в РФ подтверждён adjacent legal-AI слой через `t.me/AIlawer_bot` и `ailawyer.ru`

### Monetization verdict по сценариям
- self-serve solo lawyer: **FAIL**
- usage-based summaries: **FAIL**
- seat-based legal copilot: **FAIL**
- enterprise claims-intelligence workflow: **PASS**

### TAM / SAM / SOM
- TAM: **2,4 млрд ₽/год**
- SAM: **720 млн ₽/год**
- SOM: **60 млн ₽/год**

### Ограничения
- mandatory `localhost:9001/multi-demand` check вернул **Connection refused**
- в РФ пока нет сильного публичного claims-intelligence category leader
- высокий чек реалистичен только в enterprise / insurer / multi-office motion

---

## Stage 2. Economics

### Verdict
**PASS**

### ICP
- enterprise plaintiff practices
- insurer / claims departments
- multi-office litigation boutiques
- крупные страховые dispute teams

### Ключевые метрики
| Метрика | Значение |
|---|---:|
| Net price | **900 000 ₽/клиент/мес** |
| COGS | **250 000 ₽/клиент/мес** |
| Contribution | **650 000 ₽/клиент/мес** |
| Blended CAC | **1 680 000 ₽** |
| Monthly churn | **1,5%** |
| LTV | **43,3 млн ₽** |
| LTV/CAC | **25,8x** |
| CAC payback | **2,6 месяца** |
| Contribution margin | **72,2%** |
| Fixed costs | **4,53 млн ₽/мес** |
| Break-even | **7 клиентов**, **8-й месяц** |

### Business process lead -> first payment
| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target account list | SDR + founder | CRM, LinkedIn, legal directories | 6 ч | 18 000 | 70% |
| 2 | Персонализированный outbound | SDR | Email sequencing, Telegram, CRM | 10 дней | 110 000 | 65% |
| 3 | Qualification call | AE + founder | Zoom/Meet, CRM | 1 ч | 22 000 | 55% |
| 4 | Discovery и demo | AE + product lead | Demo env, deck, CRM | 1,5 ч | 38 000 | 40% |
| 5 | Scoping | Solutions lead + legal ops lead | Security docs, Notion/Jira | 1 неделя | 95 000 | 35% |
| 6 | Pilot proposal / ROI case | AE + founder + finance | Proposal docs, ROI calculator | 3 дня | 85 000 | 45% |
| 7 | Pilot setup | Implementation manager + ML engineer | OCR/LLM pipeline, connectors | 2 недели | 210 000 | 50% |
| 8 | Human QA и chronology review | Legal ops reviewer + product lead | Review console | 2 недели | 260 000 | 30% |
| 9 | Procurement и legal | Founder + ops/legal | Contracting, e-sign | 3 недели | 140 000 | 25% |
| 10 | Close won / handoff | AE + CSM | CRM, handoff checklist | 1 день | 42 000 | 60% |
| 11 | Production onboarding | CSM + implementation manager | LMS, help center | 1 неделя | 95 000 | 55% |
| 12 | First production batch | Legal ops + ML engineer | Monitoring, review queue | 3 дня | 110 000 | 45% |
| 13 | Invoice / collection / reconciliation | Finance ops | Billing, bank, accounting | 3 дня | 15 000 | 80% |

**Direct lead -> first payment cost: ~1,24 млн ₽.**

### Economics conclusion
Экономика проходит только в enterprise workflow SKU. Low-end версии категории не соответствуют фондовому профилю.

---

## Stage 3. Critic

### Verdict
**PASS С ОГОВОРКАМИ**

### 12-month base case
- month-12 MRR: **9,16 млн ₽**
- month-12 EBITDA: **2,09 млн ₽**
- operating break-even: **месяц 8**
- startup capital to BEP: **21,2 млн ₽**, комфортно **22-23 млн ₽**

### Scenario range
- optimistic EBITDA month 12: **3,74 млн ₽**, break-even **месяц 7**
- pessimistic EBITDA month 12: **0,11 млн ₽**, break-even **месяц 12**

### Sensitivity
- CAC x2: payback **5,17 месяца**, startup capital **30,1 млн ₽**
- churn x2: LTV **21,7 млн ₽**, month-12 EBITDA **1,60 млн ₽**
- price -30%: break-even clients **11,9**, month-12 EBITDA **-0,66 млн ₽**

### Главная критика
Фондовый риск сидит не в headline LTV/CAC, а в сочетании:
1. **price compression** вниз к seat-based/legal-copilot якорям;
2. **enterprise sales cycle** с длинными пилотами и procurement;
3. **custom services creep**, если внедрение становится полуконсалтингом.

### Kill conditions
- к месяцу 6 меньше **3 платящих клиентов** или pipeline < **6 enterprise opportunities**;
- blended CAC > **3,3 млн ₽** два квартала подряд;
- net price < **700 000 ₽/мес** при COGS > **320 000 ₽/клиент/мес**.

---

## Stage 4. Final verdict

### Score table
| Критерий | Score |
|---|---:|
| Demand / category proof | **78** |
| Monetization quality | **74** |
| Unit economics | **86** |
| Go-to-market feasibility | **66** |
| Defensibility / moat | **69** |
| Execution risk / capital efficiency | **65** |
| **Итог** | **73 / 100** |

### Финальный статус
**APPROVED С ЗАМЕЧАНИЯМИ**

### Почему approved
- есть сильный западный category proof;
- enterprise unit economics инвестиционно сильные;
- в РФ есть GEO-gap и реальный adjacent buyer behavior.

### Почему только with notes
- нужен жёсткий price floor **700-900 тыс. ₽/мес**;
- delivery нельзя превращать в кастомный legal ops service;
- repeatability enterprise sales должна быть доказана быстро.

### Top-3 risks
| Риск | Вероятность | Impact |
|---|---|---:|
| Price compression | Высокая | **2 750 000 ₽/мес** |
| Длинный enterprise sales cycle | Высокая | **1 680 000 ₽/мес** |
| Custom services creep | Средняя | **1 200 000 ₽/мес** |

### Комитетское решение
Одобрять только как **high-ticket productized enterprise workflow**. Не одобрять, если стратегия смещается в self-serve, low-ticket seats или service-heavy delivery.

---

## Stage 5. Score trajectory

### Последняя запись
2026-04-18, Program 7 / Critic and Verdict:
- решение: **APPROVED С ЗАМЕЧАНИЯМИ**
- итоговый балл: **73/100**
- ключевые метрики: CAC **1,68 млн ₽**, LTV **43,3 млн ₽**, LTV/CAC **25,8x**, payback **2,6 месяца**, break-even **7 клиентов / 8-й месяц**, startup capital **21,2 млн ₽**

### Итог траектории
Кейс прошёл путь `brief -> demand -> economics -> critic -> verdict` как enterprise-only GEO-EXPAND opportunity. Слабое место одно и то же на всех стадиях: цена, sales cycle и риск сервисизации. Сильное место тоже стабильно: доказанный buyer-job и очень сильная enterprise unit economics при правильной упаковке.

---

## Files used
- `pipeline/cases/evenup-claims-intelligence/00-brief.md`
- `pipeline/cases/evenup-claims-intelligence/02-demand.md`
- `pipeline/cases/evenup-claims-intelligence/04-economics.md`
- `pipeline/cases/evenup-claims-intelligence/05-critic.md`
- `pipeline/cases/evenup-claims-intelligence/06-verdict.md`
- `pipeline/cases/evenup-claims-intelligence/07-score-trajectory.md`
