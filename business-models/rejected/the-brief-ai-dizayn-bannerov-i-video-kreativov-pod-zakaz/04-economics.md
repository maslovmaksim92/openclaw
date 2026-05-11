# Unit Economics — The Brief AI

## Executive summary
- **Модель для расчета:** white-label / managed creative pod для performance-агентств и in-house e-commerce команд.
- **Опорный тариф:** **120 000 ₽/клиент/мес** за пакет баннеров, ресайзов, HTML5 и видео-креативов с SLA.
- **Сегмент:** **mid-market B2B, ближе к enterprise service sale**, потому что продажа идет через несколько касаний, тестовое задание, пилот и согласование SLA.
- **COGS на 1 клиента/мес:** **38 000 ₽**.
- **Contribution Margin на 1 клиента:** **82 000 ₽/мес** или **68,3%**.
- **Blended fully-loaded CAC:** **520 000 ₽**.
- **Churn benchmark:** **3,8% в месяц** как ориентир для B2B subscription/services. Источник-бенчмарк: Recurly указывает средний churn **3,8%** для B2B verticals `Software` и `Business & Professional Services`.
- **LTV:** **2 156 842 ₽** = 120 000 × 68,3% / 3,8%.
- **LTV/CAC:** **4,15x**.
- **CAC Payback:** **6,3 мес** = 520 000 / 82 000.
- **Break-even:** **47 клиентов** по accounting P&L, а для **EBITDA > 500k ₽/мес нужно ~53 клиента**.
- **Инвест-вывод:** на уровне клиента экономика приемлемая, но на уровне компании кейс **не проходит Profit Gate**, потому что при 50 клиентах EBITDA еще ниже 500k ₽/мес.

---

## 1. Подробный business process: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-списка агентств и e-com команд | SDR | HH, Рейтинг Рунета, Telegram, Google Sheets/CRM | 20 мин/аккаунт | 250 | Низкая |
| 2 | Outbound outreach: email/Telegram/LinkedIn/формы | SDR | amoCRM, почта, Telegram, sequencer | 15 мин/контакт | 180 | Средняя |
| 3 | Первичный ответ и квалификация | SDR | amoCRM, Telegram, call | 20 мин/лид | 240 | Средняя |
| 4 | Discovery-call по текущему creative workflow | AE + founder | Meet/Zoom, Notion, CRM | 45 мин | 1 600 | Низкая |
| 5 | Аудит текущих креативов и оценка SLA | Creative lead | Figma, ad libraries, Notion | 90 мин | 2 200 | Низкая |
| 6 | Коммерческое предложение и scope | AE + founder | CRM, Google Docs/PDF | 60 мин | 1 900 | Низкая |
| 7 | Пилот / тестовое производство 3-5 креативов | Designer + motion/html5 + QA | Figma, Adobe/CapCut/After Effects, AI tools | 4-6 часов | 6 500 | Средняя |
| 8 | Согласование договора и SLA | Founder + AE | Диадок/договоры/email | 3-7 дней cycle time | 3 000 | Низкая |
| 9 | Выставление счета | Ops/finance | МойСклад/банк/1С/light accounting | 15 мин | 250 | Высокая |
| 10 | Оплата и активация клиента | Finance + CSM | Банк, CRM | 1 день | 150 | Высокая |
| 11 | Онбординг: бренд-кит, доступы, шаблоны | CSM + creative lead | Notion, Figma, Drive | 2,5 часа | 4 200 | Средняя |
| 12 | Еженедельный production batch | Designers + motion/html5 + QA | Figma, HTML5 tools, video tools, AI stack | 6-8 часов/нед | 28 000/мес | Средняя |
| 13 | Отправка пачек, правки, SLA-коммуникация | CSM + QA | Telegram, email, CRM | 2 часа/нед | 6 000/мес | Средняя |
| 14 | Ежемесячный отчет и продление | CSM + AE | CRM, report template | 45 мин/мес | 1 300/мес | Средняя |
| 15 | Повторное выставление счета / предоплата | Finance | Банк/1С | 15 мин/мес | 250/мес | Высокая |

### Вывод по процессу
- Узкое место не в генерации картинок, а в **qualified sales + pilot + account management + правки**.
- Поэтому у кейса **не software CAC**, а **service-heavy CAC**.
- Маржа держится только если продукт продается как **retainer с SLA**, а не как поштучный баннерный аутсорс.

---

## 2. COGS breakdown на 1 клиента / месяц

### Базовый пакет
- 25-35 статичных баннеров/ресайзов
- 2-4 HTML5 креатива
- 2-3 коротких видео/адаптации
- turnaround 24-72 часа

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Designer labor allocation | 16 000 | ~0,35 FTE дизайнера при loaded cost ~46k/клиентской загрузке |
| Motion/HTML5 labor allocation | 7 000 | доля специалиста на видео/HTML5 |
| QA / production ops | 4 000 | проверка форматов, выгрузка, ресайзы |
| CSM / revisions allocation | 5 000 | коммуникация, правки, weekly delivery |
| AI/media tools variable share | 3 500 | Figma/Adobe/video/AI stack на клиента |
| Cloud/storage/render share | 1 500 | хранение ассетов, рендеры, CDN/облако |
| Payment leakage / admin variable | 1 000 | эквайринг, документооборот, мелкий саппорт |
| **Итого COGS** | **38 000** |  |

### Валовая экономика на клиента
- **MRR/client = 120 000 ₽**
- **COGS/client = 38 000 ₽**
- **Contribution/client = 82 000 ₽**
- **Contribution Margin = 68,3%**

Это достаточно хорошо для productized service, но ниже top-tier SaaS. Для инвестфонда это приемлемо только если churn и CAC контролируются.

---

## 3. CAC по каналам с funnel conversion

## 3.1 Raw channel CAC
| Канал | Верх воронки | Meeting rate | Proposal/Pilot | Paid conversion | New paying customers/мес | Spend, ₽/мес | Raw CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Referrals / agency partners | 40 интро | 30% | 50% в пилот | 50% из пилота | 1,5 | 210 000 | 140 000 |
| Outbound | 1 200 target accounts | 8% reply, 25% meeting | 33% в пилот | 40% close | 0,8 | 408 000 | 510 000 |
| Paid ads (Яндекс.Директ/VK/retargeting) | 320 clicks | 7,5% lead, 33% meeting | 37,5% proposal | 50% close | 0,5 | 240 000 | 480 000 |
| **Blended raw** | — | — | — | — | **2,8** | **858 000** | **306 429** |

## 3.2 Fully-loaded CAC (обязательный расчет)
Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Tools/CRM + Events + Multiplier_overhead) / New paying customers`

### Таблица fully-loaded CAC
| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 120 000 | поисковый спрос + ретаргетинг + lookalike | T1, T5 |
| Outbound team FOT (SDR/AE attributed to new) | 408 000 | SDR 160k + бонус 15% + 30% взносы; AE 280k + 8% комиссия + 30% взносы; 70% времени на new logo | T2 |
| Marketing team FOT (partial allocation) | 90 000 | founder/creative lead content + кейсы, 0,25 FTE | estimate from team plan |
| Tools (CRM, sequencing, телефония, data) | 25 000 | amoCRM + телефония + enrichment + forms | T4 |
| Events/partnerships | 55 000 | meetups, партнерские комиссии, demo-days | T3 + estimate |
| Raw acquisition spend | **698 000** | сумма строк выше |  |
| Overhead multiplier | **+419 000** | raw CAC × 1,6 для mid-market B2B с пилотом, длинным cycle и множеством касаний | T6 + analyst estimate |
| **Fully-loaded acquisition spend** | **1 117 000** |  |  |
| **New paying customers / мес** | **2,15** | blended with conservative close rate after pilot | internal model |
| **Fully-loaded CAC** | **520 000** | 1 117 000 / 2,15 |  |

### Проверка на sanity
- Сегмент не self-serve. Здесь неуместен multiplier ×1,3.
- Для **mid-market / agency pod** разумен multiplier **×1,5-1,7**. Я взял **×1,6**.
- Полученный **520k ₽ CAC** лежит внутри sanity-band для сложных B2B продаж в РФ, хотя ближе к нижней границе enterprise-like service.
- Если считать CAC только как ad spend, модель будет искусственно красивой и неверной.

---

## 4. LTV и churn

### Churn benchmark
- В качестве внешнего бенчмарка беру **3,8% monthly churn** для B2B subscription/service verticals.
- Это не идеальный peer для creative service, но он лучше отражает **retainer economics**, чем benchmark по B2C SaaS.
- Источник: Recurly, `Customer churn benchmarks`, где B2B software и business/professional services показаны на уровне **3,8%**.

### Расчет
- **Gross margin / contribution margin = 68,3%**
- **ARPA = 120 000 ₽/мес**
- **Monthly churn = 3,8%**
- **Expected lifetime = 1 / 0,038 = 26,3 мес**
- **LTV = ARPA × CM% / churn = 120 000 × 0,683 / 0,038 = 2 156 842 ₽**

Я отдельно добавляю conservative haircut 20% на нестабильность агентских бюджетов:
- **Risk-adjusted LTV = 1 725 474 ₽**

### Интерпретация
- Без удержания через SLA, шаблоны и deep account fit churn легко уедет к **5-6%/мес**, и тогда LTV резко проседает.
- При churn **5,5%/мес** LTV был бы уже **1,49 млн ₽** без haircut, что заметно хуже.

---

## 5. LTV/CAC ratio

### Базовый расчет
- **LTV/CAC = 2 156 842 / 520 000 = 4,15x**

### Risk-adjusted расчет
- **Risk-adjusted LTV/CAC = 1 725 474 / 520 000 = 3,32x**

### Вывод
- Даже после risk haircut показатель остается **выше 3:1**.
- Значит кейс проходит **investment-grade threshold**, но без большого запаса.
- Если blended price упадет ниже **105k ₽/мес** или churn поднимется выше **5%/мес**, инвестиционный профиль быстро ломается.

---

## 6. CAC Payback

Формула по требованию:

`CAC Payback = CAC / MRR_per_customer`

Но для управленческого смысла я показываю обе версии.

| Метрика | Формула | Значение |
|---|---|---:|
| Simple CAC Payback | 520 000 / 120 000 | **4,3 мес** |
| Contribution CAC Payback | 520 000 / 82 000 | **6,3 мес** |

### Вывод
- Даже contribution-based payback **< 12 мес**, значит канал окупаемый.
- Для service-heavy B2B это хорошо, но не феноменально.

---

## 7. Contribution Margin %

| Показатель | ₽ |
|---|---:|
| Revenue/client/month | 120 000 |
| COGS/client/month | 38 000 |
| Contribution/client/month | 82 000 |
| **Contribution Margin %** | **68,3%** |

Это верхняя часть допустимого диапазона для productized creative service. Для обычного агентства это хорошо, для SaaS это средне.

---

## 8. Team & FOT

## 8.1 Таблица найма
| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO / Tech Lead | 1 | 500 000 | 2 | 2 | 150 000 | 650 000 |
| Senior Backend | 1 | 380 000 | 1,5 | 1,5 | 114 000 | 494 000 |
| Frontend | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |
| ML Engineer | 0 | 0 | — | — | — | 0 |
| DevOps | 0,5 outsource | 180 000 | 1 | 1 | 54 000 | 234 000 |
| SDR (outbound) | 1 | 184 000 | 0,5 | 1 | 55 200 | 239 200 |
| AE (Account Exec) | 1 | 302 400 | 1,5 | 2,5 | 90 720 | 393 120 |
| Customer Success | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| Creative Lead / PM | 1 | 240 000 | 1 | 1 | 72 000 | 312 000 |
| Designers | 4 | 170 000 | 0,5-1 | 1 | 51 000 | 884 000 |
| Motion / HTML5 specialist | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |
| QA / Production Ops | 1 | 160 000 | 0,5 | 1 | 48 000 | 208 000 |
| Finance / back office outsource | 1 | 90 000 | 0,5 | 0,5 | included | 90 000 |
| **Итого full team monthly** | **13,5 FTE** | — | — | — | — | **5 285 320 ₽** |

### Комментарий по структуре команды
- Для этого кейса **не нужен внутренний ML R&D team** на ранней стадии. Core value не в foundation model, а в workflow, SLA и creative ops.
- Поэтому ML hire = 0, иначе экономика станет хуже без прироста выручки.
- Часть creative team должна сидеть в **COGS**, а не во fixed OPEX. Иначе break-even будет выглядеть хуже, чем есть на практике.

## 8.2 Разделение FOT на fixed vs variable

### Fixed team / SG&A + product
| Блок | ₽/мес |
|---|---:|
| CEO | 845 000 |
| CTO | 650 000 |
| Backend | 494 000 |
| Frontend | 364 000 |
| 0,5 DevOps | 234 000 |
| SDR | 239 200 |
| AE | 393 120 |
| Finance/back-office | 90 000 |
| **Fixed FOT subtotal** | **3 309 320** |

### Variable / client-serving team, входит в COGS
| Блок | ₽/мес при полной команде |
|---|---:|
| CSM | 286 000 |
| Creative lead / PM | 312 000 |
| Designers x4 | 884 000 |
| Motion / HTML5 | 286 000 |
| QA / production ops | 208 000 |
| **Variable service FOT** | **1 976 000** |

---

## 9. Fixed costs breakdown

| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| Fixed FOT (см. выше) | 3 309 320 | founder + product + sales + admin |
| Office / coworking / legal / accounting overhead | 180 000 | гибридная команда, без большого офиса |
| Core SaaS tools | 95 000 | CRM, workspace, телефония, docs |
| R&D cloud / infra | 120 000 | backend, hosting, file storage |
| Recruiting / employer brand reserve | 60 000 | needed because hiring is not instant |
| Travel / partner meetings / misc | 55 000 | клиентские встречи, demo travel |
| **Total fixed costs / month** | **3 819 320 ₽** |  |

---

## 10. Break-even по количеству клиентов и по месяцу

### 10.1 Break-even by client count
- **Contribution per client = 82 000 ₽/мес**
- **Fixed costs = 3 819 320 ₽/мес**
- **Break-even clients = 3 819 320 / 82 000 = 46,6**

Округляю до:
- **47 клиентов для accounting break-even**
- **53 клиента для EBITDA > 500k ₽/мес**

### Проверка правила Profit Gate
- При **50 клиентах**:
  - Revenue = **6 000 000 ₽/мес**
  - COGS = **1 900 000 ₽/мес**
  - Contribution = **4 100 000 ₽/мес**
  - EBITDA ≈ **280 680 ₽/мес**

На этом уровне **порог 500k EBITDA еще не достигнут**.

- При **53 клиентах**:
  - Revenue = **6 360 000 ₽/мес**
  - COGS = **2 014 000 ₽/мес**
  - Contribution = **4 346 000 ₽/мес**
  - EBITDA ≈ **526 680 ₽/мес**

### Интерпретация
- Формально кейс **не ломается**, но запас прочности слабый: чтобы выйти на EBITDA 500k+, нужно примерно **53 платящих клиента**.
- Это высокое требование для service-heavy компании.

## 10.2 Break-even by month: ramp model

### Допущения по клиентскому росту
| Месяц | Платящие клиенты на конец месяца |
|---|---:|
| M1 | 0 |
| M2 | 1 |
| M3 | 2 |
| M4 | 4 |
| M5 | 7 |
| M6 | 11 |
| M7 | 16 |
| M8 | 22 |
| M9 | 29 |
| M10 | 37 |
| M11 | 46 |
| M12 | 53 |

### Cumulative FOT timeline M1-M12
| Month | Кто уже в команде | FOT monthly, ₽ | Комментарий |
|---|---|---:|---|
| M1 | CEO, 1 designer, fractional ops | 1 169 000 | lean setup, без mass hiring |
| M2 | + SDR, + second designer | 1 642 200 | outbound starts |
| M3 | + frontend, + creative lead | 2 318 200 | first workflow tooling |
| M4 | + AE, + QA | 2 919 320 | first pilots |
| M5 | + backend | 3 413 320 | client portal/light automation |
| M6 | + CSM, + motion/html5 | 4 011 320 | service layer stabilizes |
| M7 | + CTO | 4 661 320 | product and ops hardening |
| M8 | + third designer | 4 882 320 | capacity expansion |
| M9 | + fourth designer | 5 103 320 |  |
| M10 | + 0,5 DevOps | 5 285 320 | near full team |
| M11 | full team | 5 285 320 |  |
| M12 | full team | 5 285 320 |  |

### Burn-to-breakeven
| Month | Clients | Revenue, ₽ | Contribution, ₽ | Fixed+nonclient costs, ₽ | EBITDA / burn, ₽ |
|---|---:|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | 1 450 000 | -1 450 000 |
| M2 | 1 | 120 000 | 82 000 | 1 930 000 | -1 848 000 |
| M3 | 2 | 240 000 | 164 000 | 2 560 000 | -2 396 000 |
| M4 | 4 | 480 000 | 328 000 | 3 160 000 | -2 832 000 |
| M5 | 7 | 840 000 | 574 000 | 3 670 000 | -3 096 000 |
| M6 | 11 | 1 320 000 | 902 000 | 4 250 000 | -3 348 000 |
| M7 | 16 | 1 920 000 | 1 312 000 | 4 930 000 | -3 618 000 |
| M8 | 22 | 2 640 000 | 1 804 000 | 5 120 000 | -3 316 000 |
| M9 | 29 | 3 480 000 | 2 378 000 | 5 320 000 | -2 942 000 |
| M10 | 37 | 4 440 000 | 3 034 000 | 5 500 000 | -2 466 000 |
| M11 | 46 | 5 520 000 | 3 772 000 | 5 680 000 | -1 908 000 |
| M12 | 53 | 6 360 000 | 4 346 000 | 5 820 000 | -1 474 000 |

### Что видно
- При aggressive team build до M12 чистый burn остается тяжелым.
- Значит проекту нужен либо:
  1. более медленный hiring,
  2. более высокий ARPA 140-160k ₽,
  3. или больше партнерских продаж вместо paid.

Иначе операционно компания может иметь хорошие unit economics, но **слабую capital efficiency**.

---

## 11. Cash runway

### Допущение
- **startup_capital = 25 000 000 ₽**

### Расчет
- Средний monthly burn на M1-M12 ≈ **2,73 млн ₽/мес**.
- **Cash runway = 25,0 / 2,73 = 9,2 месяца**.

### Вывод
- Для такого GTM и hire-plan **25 млн ₽ недостаточно**, если строить полную команду заранее.
- Более реалистично:
  - стартовать с 12-15 млн ₽ и очень lean team,
  - не собирать full-stack product squad до подтверждения retention,
  - держать founders-led sales минимум 6 месяцев.

---

## 12. Sanity checks

### Проверка 1. CAC Payback
- Simple payback **4,3 мес** < 12 мес, PASS.
- Contribution payback **6,3 мес** < 12 мес, PASS.

### Проверка 2. LTV/CAC
- Base **4,15x**, risk-adjusted **3,32x**. PASS.

### Проверка 3. CAC vs benchmark
- Полученный CAC **520k ₽** не выглядит заниженным для service-heavy B2B sale.
- Ниже 30% от benchmark он не падает, red flag нет.

### Проверка 4. Hiring realism
- В M1 не нанимается 5+ человек, значит time-to-hire не нарушен.
- Full FOT > 5M ₽/мес при команде 13,5 FTE, это реалистично.
- Это и есть главный контрсигнал: сервис оказывается капиталоемким сильнее, чем выглядит из demand-stage.

---

## 13. Final economics verdict

### Что нравится
- Чек **120k ₽/мес** поддерживается спросом из white-label agency pod сегмента.
- **LTV/CAC выше 3:1**, payback вменяемый.
- Contribution margin **68%+** позволяет строить хороший retainer business.

### Что не нравится
- Break-even наступает слишком поздно и требует **47 клиентов**, а для EBITDA >500k нужно примерно **53 клиента**.
- Hiring plan и burn тяжелые, если компания пытается параллельно строить внутренний продукт и service layer.
- Это **не легкий SaaS**, а трудоемкий operations business с software wrapper.

## Итог
- **Unit economics: FAIL на company level при текущем hire-plan.**
- **Investment fund view:** клиентская юнит-экономика выглядит терпимо, но company economics не выдерживает жесткий profit gate.
- Если founders не докажут более высокий ARPA, меньшую команду или иную delivery-модель, кейс не подходит под инвесткомитет.

## Sources
- T1. Яндекс.Директ, настройки бюджета и CPC logic: https://yandex.ru/support/direct/ru/strategies/average-cpc
- T2. HH.ru, рыночные вилки по backend / frontend / ML / sales в Москве, 2026 search snapshots: https://hh.ru/vacancies/senior-backend-developer ; https://hh.ru/vacancies/machine-learning-engineer ; https://hh.ru/vacancies/senior-frontend-developer
- T3. Рейтинг Рунета performance agencies 2025: https://ratingruneta.ru/performance/
- T4. amoCRM pricing: https://www.amocrm.ru/buy/tariff/
- T5. Demand-stage evidence and market references from 02-demand.md in this case
- T6. Paddle on CAC needing wage/overhead inclusion in benchmarks: https://www.paddle.com/resources/saas-benchmarks
- T7. Recurly churn benchmarks: https://recurly.com/research/churn-rate-benchmarks
