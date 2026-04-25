[HEALTHCARE] Webiomed — APPROVED WITH NOTES: 71/100 | EBITDA base=4154К₽/мес через 24 мес | LTV/CAC=9,7x | Ключевое преимущество: regulated document QA + clinical workflow встраивается в ЭМК | Главный риск: price compression и project-heavy внедрение.

# Webiomed healthcare document AI v2 — 06-verdict
sector: HEALTHCARE
status: APPROVED WITH NOTES
score: 71/100
date: 2026-04-25
slug: webiomed-healthcare-document-ai-v2
repo_path: approved/webiomed-healthcare-document-ai-v2/verdict.md

## Итог
**Вердикт инвесткомитета: APPROVED WITH NOTES.**

Кейс проходит approval gate, потому что одновременно выполняются два условия:
1. **Normalized score = 71/100**, то есть выше порога 70.
2. **company_ebitda_potential_rub_month = 4 154 000 ₽/мес** достижима при **50 клиентах** и на горизонте **до 24 месяцев**, что проходит обязательный profitability gate.

Это не простой AI-wrapper, а regulated healthcare workflow с реальной локальной выручкой, понятным buyer motion и сильной unit economics. Но approval даётся с оговорками: рынок остаётся sales-led, pricing очень чувствителен, а enterprise rollout легко превращается в тяжёлый интеграционный сервис.

## Этапы 1-5
### Этап 1 — Intake
Исходный wedge: Webiomed продаёт клиникам и региональным медсистемам AI-слой для контроля качества медицинской документации, клинических подсказок и снижения ошибок в ЭМК без найма дополнительного ручного аудита.

### Этап 2 — Validation / Evidence
Фактическая валидация категории уже есть:
- продукт Webiomed.DocReviewer проверяет качество меддокументов и формирует отчёт за **5–15 секунд**;
- компания уже вышла в контур коммерческой медицины;
- по публичным источникам у ООО «К-Скай» была выручка **142,4 млн ₽** в 2024 году и **103,1 млн ₽** в 2025 году, то есть buyer в РФ уже платит не только за пилоты;
- наличие регистрационного удостоверения и внедрений в десятках регионов снижает регуляторный риск.

### Этап 3 — Demand
Demand-stage опирается на файл `02-demand.md`, потому что отдельный `03-demand.md` в кейсе отсутствует.
Публичный exact-search спрос низкий, но B2B/B2G budget line подтверждена:
- рынок AI в российской медицине оценён в **12 млрд ₽**;
- SAM по кейсу сходится в коридоре **1,21–1,32 млрд ₽**;
- buyer universe состоит из крупных частных сетей, диагностических групп и региональных цифровых контуров;
- willingness to pay подтверждена открытыми price anchors аналогов и реальной выручкой Webiomed.

### Этап 4 — Economics
Базовая экономика strong enough for IC:
- customer_ltv_rub = **7 320 000 ₽**
- CAC = **758 000 ₽**
- LTV/CAC = **9,7x**
- CAC payback = **3,0 мес по revenue / 4,1 мес по contribution**
- Gross Margin = **73,2%**
- contribution_margin_rub_month = **183 000 ₽/мес**
- fixed_costs_rub_month = **5 896 000 ₽/мес**
- startup_capital_to_bep_rub = **38 094 203 ₽**

### Этап 5 — Critic / Finance Risk
PnL проходит, но хвостовые риски значимы:
- base M12 EBITDA = **-791 610 ₽/мес**
- Monte Carlo Lite: **p10 EBITDA @M24 = -1,2 млн ₽/мес**, **p50 = 3,4 млн ₽/мес**, **p90 = 8,2 млн ₽/мес**
- наиболее опасные sensitivity-факторы: **price -30%** и **CAC x2**

## Оценка
Source tier balance: T1=1, T2=11, T3=2, weighted=1.93. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | «LTV/CAC = 9,7x», «CAC Payback = 3,0 месяца», «Contribution Margin = 73,2%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 21 | «При 50 клиентах EBITDA > 500 000 ₽/мес достижима», base-case даёт «порядка 4,1–4,4 млн ₽ EBITDA/мес». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 15 | «SAM bottom-up = 1,2096 млрд ₽», но internal demand check вернул «LOW» и tier-balance даёт штраф -5. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 16 | «контроль качества меддокументов», «API», «регистрационное удостоверение» и интеграция в ЭМК создают moat выше среднего. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 14 | «p10 EBITDA < 0», есть риск «project-heavy delivery», санкции, 152-ФЗ и зависимость от внешних LLM/API. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | «Партнёры / интеграторы МИС» дают лучший CAC, а ICP и named-target GTM уже явно сформулированы. |

**Сумма raw:** 107/150  
**Normalized score = round((107 × 100) / 150) = 71/100**

## 7-factor moat framework
| Фактор | Балл (0-3) | Почему |
|---|---:|---|
| Network effects | 1 | Каждый новый клиент почти не усиливает продукт для остальных напрямую. |
| Switching costs | 3 | Данные, интеграции в МИС/ЭМК, обучение врачей и внутренние quality-процессы делают замену болезненной. |
| Scale economies | 2 | Shared infra, compliance и model ops улучшаются с ростом, хотя integration still partly custom. |
| Proprietary data / model advantage | 2 | Есть доступ к медицинским документам и накопленной clinical логике, но публичного доказательства размера датасета мало. |
| Regulatory moat | 3 | Регуляторная упаковка, медконтур, регистрационное удостоверение и data residency дают серьёзный барьер входа. |
| Brand / distribution | 2 | Webiomed заметен в локальном healthtech-контуре, но не монополист. |
| Embedded workflow | 3 | Решение сидит прямо в процессе ведения ЭМК, аудита и clinical guidance. |

**Moat raw = 16/21**  
**Moat score = round((16 × 25) / 21) = 19/25**

Комментарий: формальный 7-factor score тянет на 19/25, но итоговый rubric score по критерию #4 снижен до **16/25**, потому что moat пока сильнее в regulated workflow, чем в company-exclusive data flywheel.

## Investment committee view
### Почему кейс прошёл
1. **Есть локальная монетизация и category proof в РФ.**
2. **Unit economics сильная даже с консервативным churn.**
3. **EBITDA gate выполняется** при <50 клиентах и горизонте до 24 месяцев.
4. **Регуляторика и интеграции** создают защиту лучше, чем у generic AI-сервисов.

### Почему кейс не получил чистый APPROVED
1. Exact-demand по поисковому следу низкий.
2. Monte Carlo даёт отрицательный p10.
3. Price compression и integration drag могут быстро ухудшить модель.

## Полный бизнес-процесс из 04-economics.md
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ на 1 нового клиента | Уровень автоматизации |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-листа клиник и сетей | SDR | hh/рынок, сайт клиники, CRM | 0,5 дня | 4 000 | средний |
| 2 | Outreach по email/телефону/партнёрам | SDR | amoCRM, телефония, почта | 10-14 дней | 18 000 | средний |
| 3 | Qualification call | SDR + AE | CRM, скрипты, Zoom/Meet | 3-5 дней | 14 000 | средний |
| 4 | Demo продукта и ROI-кейс | AE + CEO/BD | презентация, demo, калькулятор ROI | 5-7 дней | 22 000 | низкий |
| 5 | Scoping: МИС, юридические ограничения, ИБ, обезличивание данных | CTO + AE + clinical expert | чек-листы, API docs, security Q&A | 1-2 недели | 36 000 | низкий |
| 6 | Подготовка pilot proposal и коммерческого предложения | AE + CEO | шаблон КП, калькуляция, CRM | 3-5 дней | 21 000 | средний |
| 7 | Pilot / интеграция / подключение | CTO + backend + ML + CSM | API, sandbox, мониторинг | 3-6 недель | 96 000 | низкий |
| 8 | Review результатов пилота, закупочный комитет | AE + CEO + clinical champion | отчёт по качеству, ROI summary | 1-2 недели | 31 000 | низкий |
| 9 | Договор, DPA, ИБ/legal согласование | CEO + ops/legal | ЭДО, шаблоны договора | 2-4 недели | 29 000 | средний |
| 10 | Выставление счёта, onboarding, запуск recurring payment | ops + CSM + finance | CRM, 1С/ЭДО, банк | 3-5 дней | 18 000 | высокий |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 7 320 000 ₽ |
| CAC | 758 000 ₽ |
| LTV/CAC | 9,7x |
| CAC Payback | 3,0 мес revenue / 4,1 мес contribution |
| Gross Margin | 73,2% |
| contribution_margin_rub_month | 183 000 ₽/мес |
| fixed_costs_rub_month | 5 896 000 ₽/мес |
| Break-even clients | 33 |
| clients_to_500k_ebitda | 35 |
| clients_to_1m_ebitda | 38 |
| months_to_500k_ebitda | 15 |
| months_to_1m_ebitda | 16 |
| company_ebitda_rub_month base | 4 154 000 ₽/мес при 50 клиентах |
| company_ebitda_potential_rub_month | 4 154 000 ₽/мес |
| startup_capital_to_bep_rub | 38 094 203 ₽ |

## Команда
| Роль | Функция | FOT fully-loaded ₽/мес |
|---|---|---:|
| CEO | продажи top accounts, fundraising, legal, partnerships | 845 000 |
| CTO / Tech Lead | архитектура, ИБ, интеграции с МИС | 715 000 |
| Senior Backend #1 | API, backend, integrations | 520 000 |
| Senior Backend #2 | data pipelines, backend features | 520 000 |
| ML Engineer | NLP/LLM quality, extraction, evaluation | 650 000 |
| DevOps | infra, monitoring, CI/CD, security hardening | 455 000 |
| Frontend | кабинеты, UX для клиник, dashboards | 364 000 |
| SDR | pipeline generation, outreach | 234 000 |
| AE | demo, pilot, closing | 429 000 |
| Customer Success | onboarding, adoption, renewals | 299 000 |
| Clinical expert / методист 0.5 FTE | проверка правил, quality logic, методология | 195 000 |
| **Итого** |  | **5 226 000 ₽/мес** |

## GTM — 10 named targets
| # | Название | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | МЕДСИ | крупная сеть с 145 клиниками и высокой ценой врачебного часа, где ROI от контроля ЭМК и clinical guidance наиболее понятен | email decision-maker + warm intro через digital health ecosystem | 450 000 ₽/мес |
| 2 | ГК «Мать и дитя» | много стандартизированных амбулаторных сценариев и высокий риск ошибок в документации | конференция + direct outreach к меддиректору | 350 000 ₽/мес |
| 3 | «СМ-Клиника» | большой поток амбулаторных приёмов и зрелый private-clinic workflow | email COO / CIO + follow-up после отраслевого кейса | 320 000 ₽/мес |
| 4 | EMC | premium-сегмент, где стоимость времени врача и quality assurance особенно высоки | founder-led outreach + email CMO/CIO | 300 000 ₽/мес |
| 5 | «РЖД-Медицина» | распределённая сеть и централизованный контур качества, подходящий для annual license | партнёрство с интегратором / procurement intro | 500 000 ₽/мес |
| 6 | ГК «Эксперт» | диагностические и многопрофильные центры с болью в стандартизации медзаписей | email decision-maker + отраслевая конференция | 280 000 ₽/мес |
| 7 | «Скандинавия / АВА-ПЕТЕР» | зрелая частная сеть с цифровым контуром и высокой нагрузкой на документацию | direct email + warm intro через профильные ассоциации | 300 000 ₽/мес |
| 8 | «Будь Здоров» | федеральная сеть, где экономия ручного аудита и снижение дефектов карт имеют сетевой ROI | партнёрский канал + outbound ABM | 320 000 ₽/мес |
| 9 | MedSwiss | private-clinic buyer с повторяемым outpatient workflow и понятным quality KPI | email decision-maker + тематический вебинар | 220 000 ₽/мес |
| 10 | МИАЦ/Депздрав Татарстана | региональный цифровой контур с подтверждённым интересом к AI в медицине и масштабом для B2G пилота | тендерный мониторинг + региональная конференция + партнёрство | 600 000 ₽/мес |

## Top-3 risks
| Риск | Вероятность | Impact | Почему это top-3 |
|---|---|---|---|
| Price compression и уход в более дешёвые point-solutions | high | high | Stress-case «Price -30%» уводит EBITDA @M12 до **-2 883 573 ₽**, то есть pricing power критичен. |
| Project-heavy интеграции с МИС и service creep | medium-high | high | Внедрение >8 недель и рост кастома превращают продукт в SI и съедают margin. |
| evidence_quality_unverified и низкий source-tier balance | medium | medium-high | Weighted tier balance **1.93** означает слабую долю T1-доказательств по рынку и спросу. |

## Proof points для APPROVED
1. **Есть локальная выручка:** у ООО «К-Скай» зафиксирована выручка 103,1-142,5 млн ₽ по публичным источникам за 2024-2025 годы.
2. **Есть продуктовый workflow:** DocReviewer проверяет качество меддокументов и формирует отчёт за 5–15 секунд.
3. **Есть regulatory packaging:** регистрационное удостоверение и работа в медконтуре снижают barrier risk.
4. **Есть category expansion в РФ:** рядом появляются LazyDoc, Medico Mind, Panacea Doc и iAmbulant как подтверждение отдельного document-AI сегмента.
5. **Есть EBITDA gate:** даже conservative base-case приводит к EBITDA значительно выше 500k ₽/мес при 50 клиентах.

## Что доказать в ближайшие 6 месяцев
1. **Pilot-to-paid ≥ 20%** на private-clinic ICP.
2. **Floor-price не ниже 250 000 ₽/мес** без системных скидок >20%.
3. **Стандартизированный MIS connector**, чтобы go-live укладывался в 6-8 недель.
4. **2-3 новых reference logos** вне existing network и не только в госконтуре.

## Delta vs previous
P5 существенно усилил кейс благодаря рабочей unit economics. P6 добавил risk discount: M12 ещё отрицательный, p10 по Monte Carlo ниже нуля, поэтому финальный статус не чистый APPROVED, а **APPROVED WITH NOTES**.

## Финальный комитетский вывод
**APPROVED WITH NOTES.**

Это инвестируемый vertical AI-layer для regulated healthcare в РФ, если фонд готов работать с длинным sales cycle, интеграциями и compliance-heavy delivery. Не подходит как лёгкий self-serve SaaS, но подходит как infrastructure-grade healthcare workflow с сильным LTV/CAC и понятным profitability path.


---

# Файл: 00-brief.md

# Краткий бриф

## Кейс
Webiomed, AI-контроль медицинской документации и клинические подсказки

## Почему открыт
- Сигнал локальный и коммерческий: продукт уже внедряется в РФ, имеет регуляторную упаковку и понятный ROI для клиник и региональных систем здравоохранения.
- Порог Program 1 проходит: B2B/B2G-сделки в медицине дают достаточно высокий чек, чтобы модель могла выйти на EBITDA выше 500 000 ₽ в месяц.

## Что проверить дальше
- Проверить, кто является основным покупателем: частные клиники, региональные медсистемы или федеральные сети.
- Подтвердить повторяемость выручки и глубину painkiller-эффекта: аудит, комплаенс, качество записей, клинические рекомендации.
- Оценить внедренческий цикл и реалистичность масштабирования без тяжёлого кастома.

## Следующий этап
P3-demand-validation.


---

# Файл: 01-evidence.md

# Подтверждающие сигналы

## 2026-04-22 — supporting signal
- **Источник:** https://www.comnews.ru/digital-economy/content/243369/2026-01-21/2026-w04/1012/webiomed-vnedril-ii-dlya-kontrolya-kachestva-medicinskikh-zapisey
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс тем, что показывает уже коммерчески упакованный workflow для контроля качества медицинских записей, который даёт результат за секунды и снижает нагрузку на внутренний аудит клиники. Это подтверждает, что Webiomed решает не только broad clinical analytics, но и конкретную pain-point задачу с понятным ROI для частных клиник и сетей.
- **Ключевые данные и факты:** сервис автоматически проверяет качество меддокументов и формирует подробный отчёт за 5–15 секунд; одновременно сохраняются более широкие сигналы масштаба, включая внедрение в 42 субъектах РФ, рост обращений врачей к подсказкам в 47 раз и выручку компании 142,4 млн руб. в 2024 году.


## 2026-04-23 — supporting signal — iambulant как локальное подтверждение спроса на AI-структурирование медкарт
- **Источник:** https://sk.ru/news/skolovskij-startap-iambulant-privlyok-investicii-na-razvitie-ii-platformy-dlya-strukturirovaniya-medkart/ ; https://sk.ru/news/2-mln-medicinskih-dokumentov-formiruetsya-v-cifre-ezhednevno/ ; https://sk.ru/news/ii-vas-vylechit/
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс Webiomed тем, что подтверждает наличие отдельного локального спроса на AI-сервисы, которые превращают свободный текст медкарты в структурированный цифровой профиль и сокращают время врача на рутину. Это снижает риск, что документный AI в healthcare держится на одном игроке, и показывает, что категория уже формируется как повторяемый B2B-рынок для сетей клиник.
- **Ключевые данные и факты:** iambulant привлёк 15 млн руб. инвестиций; в пилотах время работы с документацией сокращается на 30–50%; на рынке ежедневно формируется около 2 млн медицинских документов в цифре с потенциалом роста до 10 млн в сутки.

## 2026-04-23 — supporting signal — Webiomed как прямое подтверждение коммерческого document AI для клиник
- **Источник:** https://sk.ru/news/generativnyj-ii-vnedryon-v-process-proverki-kachestva-medicinskoj-dokumentacii/ ; https://sk.ru/news/rezident-skolkovo-vyvel-ii-platformu-webiomed-na-rynok-kommercheskoj-mediciny/ ; https://www.rusprofile.ru/id/7532417 ; https://www.webiomed.ru/en
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс тем, что подтверждает уже коммерциализированный workflow для автоматической проверки и исправления меддокументации, причём не только в государственном, но и в коммерческом контуре клиник. Это повышает уверенность в том, что категория document AI в healthcare в РФ имеет не только технологическую, но и платёжеспособную B2B-основу.
- **Ключевые данные и факты:** генеративный ИИ формирует отчёт по качеству меддокументов за 5–15 секунд; Webiomed выведен на рынок коммерческой медицины; выручка ООО «К-Скай» за 2024 год указана на уровне 142,455 млн ₽; официальный сайт описывает контроль ведения ЭМК и анализ медицинских записей как ключевой продуктовый контур.

## 2026-04-24 — supporting signal — Webiomed как коммерческий AI-контур для контроля качества медзаписей
- **Дата:** 2026-04-24
- **Источник:** https://www.comnews.ru/digital-economy/content/243369/2026-01-21/2026-w04/1012/webiomed-vnedril-ii-dlya-kontrolya-kachestva-medicinskikh-zapisey ; https://www.cnews.ru/news/line/2025-06-11_rezident_skolkovo_vyvel ; https://checko.ru/company/k-skay-1197746481360
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс тем, что одновременно подтверждает конкретный workflow контроля качества меддокументации, выход в коммерческую медицину и уже заметную выручку компании. Это снижает риск, что продукт остаётся только исследовательской или пилотной историей без устойчивой B2B-монетизации.
- **Ключевые данные и факты:** сервис проверки медзаписей формирует отчёт за 5–15 секунд; Webiomed выведен на рынок коммерческой медицины; по данным Checko выручка ООО «К-Скай» за 2024 год составила 142,5 млн ₽, штат 42 сотрудника и 69 госконтрактов на 304,9 млн ₽.

## 2026-04-24 — supporting signal — Webiomed как AI-контур контроля качества меддокументации
- **Дата:** 2026-04-24
- **Источник:** https://sk.ru/news/generativnyj-ii-vnedryon-v-process-proverki-kachestva-medicinskoj-dokumentacii/ ; https://sk.ru/news/rezident-skolkovo-vyvel-ii-platformu-webiomed-na-rynok-kommercheskoj-mediciny/ ; https://sk.ru/news/medicinskij-ii-pomoshnik-rezidenta-skolkovo-poluchil-registracionnoe-udostoverenie/ ; https://webiomed.ru/
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс тем, что одновременно подтверждает продуктовую зрелость workflow по проверке меддокументации, наличие коммерческого эффекта для клиник и снижение регуляторного риска за счёт регистрационного удостоверения. Это делает кейс сильнее как самостоятельный healthcare B2B-контур, а не как единичный пилот.
- **Ключевые данные и факты:** сервис формирует отчёт по качеству медицинской документации за 5–15 секунд; пилот в коммерческой медицине показал рост среднего чека на 15% и рост допобследований на 30%; обновлённая СППВР Webiomed получила регистрационное удостоверение Росздравнадзора.


## 2026-04-24 — supporting signal — LazyDoc как подтверждение спроса на ambient documentation для клиник
- **Источник:** https://www.cnews.ru/news/line/2026-01-30_dialogovyj_ii_dlya_zdravoohraneniya ; https://www.rusprofile.ru/id/1237800119754 ; https://minzdrav.gov.ru/news/2026/04/17/30794-itogovaya-kollegiya-2025-i-plany-na-2026-tsifrovaya-transformatsiya-pronizyvaet-vse-zadachi-stoyaschie-pered-otraslyu-zdravoohraneniya
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс тем, что подтверждает отдельный платёжеспособный workflow вокруг транскрибации приёма врача и автозаполнения медзаписи в российских клиниках. Это снижает риск, что document AI в healthcare остаётся нишей без повторяемого спроса, и показывает прямой ROI через экономию времени врача и сокращение рутины.
- **Ключевые данные и факты:** внедрение LazyDoc в сети клиник «Полимедика» дало до 1,5 часов экономии времени врача в день и сократило рутинные операции по заполнению документов на 80–90%; в РФ зарегистрировано юрлицо ООО «Ленивый Доктор»; Минздрав РФ в апреле 2026 года назвал цифровую трансформацию сквозным приоритетом отрасли.

## 2026-04-24 — supporting signal — Webiomed как подтверждение зрелого AI-анализа ЭМК и лабораторных данных
- **Дата:** 2026-04-24
- **Источник:** https://www.forbes.ru/healthcare/551689-vspomogatel-nyj-mehanizm-pervyj-rejting-ii-resenij-dla-mediciny ; https://webiomed.ru/products/webiomed-dhra/ ; https://webiomed.ru/novosti/kontrol-onkonastorozhenosti/
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс тем, что подтверждает не только workflow контроля документации, но и более широкий клинический контур анализа ЭМК и лабораторных данных с выявлением рисков, пропущенных скринингов и подозрений на заболевания. Это делает кейс сильнее как платформу для recurring AI-слоя в клинике, а не как узкий инструмент аудита записей.
- **Ключевые данные и факты:** Forbes указывает 142,4 млн ₽ выручки Webiomed за 2024 год и 1 место в рейтинге ИИ-решений для медицины; продуктовая страница заявляет сокращение времени обработки медкарты в 10 раз; в апреле 2026 компания добавила автоматический контроль онконастороженности и соблюдения требований по скринингу.

## 2026-04-24 — supporting signal — LazyDoc для транскрипции приёмов врача и меддокументации
- **Дата:** 2026-04-24
- **Источник:** https://www.cnews.ru/news/line/2026-01-30_dialogovyj_ii_dlya_zdravoohraneniya ; https://lazydoc.ai/ ; https://www.rusprofile.ru/id/1237800119754 ; https://minzdrav.gov.ru/en/special/news/2026/04/17/30794-itogovaya-kollegiya-2025-i-plany-na-2026-tsifrovaya-transformatsiya-pronizyvaet-vse-zadachi-stoyaschie-pered-otraslyu-zdravoohraneniya
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс по healthcare document AI, потому что подтверждает локальный спрос именно на ambient documentation и автоматизацию медзаписей в российских клиниках, а не только на общий контроль качества документации. Он снижает риск, что workflow ограничен пилотами, за счёт конкретного ROI и наличия on-premise/SaaS поставки под требования рынка РФ.
- **Ключевые данные и факты:** CNews сообщает, что внедрение LazyDoc высвободило врачам до 1,5 часов в день; сайт продукта заявляет сокращение времени на документацию до 70% и поставку в SaaS и on-premise; Rusprofile подтверждает действующее российское юрлицо; Минздрав фиксирует цифровую трансформацию здравоохранения как приоритет 2026 года.

## 2026-04-24 — supporting signal — Medico Mind как подтверждение спроса на AI-аудит меддокументации для клиник
- **Дата:** 2026-04-24
- **Источник:** https://vc.ru/ai/2745925-ii-kontrol-kachestva-i-audit-meditsinskoy-dokumentatsii-v-klinike-medico-mind ; https://medicomind.ru/for-owners ; https://medicomind.ru/pricing
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс тем, что подтверждает наличие отдельного коммерческого спроса на AI-контроль качества медицинской документации именно в частных клиниках, а не только в broader clinical analytics. Он снижает риск, что category document AI в healthcare держится на одном вендоре, и показывает повторяемую SaaS-модель с оплатой за врача или организацию.
- **Ключевые данные и факты:** Medico Mind заявляет автоматический аудит медкарт и назначений на соответствие клиническим рекомендациям и стандартам Минздрава; страница для руководителей обещает сокращение времени аудита на 40%; pricing указывает тариф 2 000 ₽ в месяц на врача и отдельную модель для организаций, что подтверждает recurring revenue-логику.


## 2026-04-24 — supporting signal — Panacea Doc как подтверждение спроса на AI-контроль медкарт и стандарта приёма
- **Дата:** 2026-04-24
- **Источник:** https://itm-ai.ru/meropriyatiya/pobediteli-konkursa-startup-pitch-na-lechebnom-delo-forume/ ; https://panaceadoc.ru/qualitycontrol ; https://companies.rbc.ru/id/1247700522070-ooo-panatseya-dok/
- **Тип:** supporting signal
- **Как усиливает кейс:** Сигнал усиливает кейс Webiomed тем, что подтверждает наличие отдельного локального спроса на AI-контроль качества медкарт, соблюдение стандартов приёма и снижение юридических рисков в клиниках. Это снижает риск, что категория держится на одном игроке, и показывает повторяемый private-clinic workflow вокруг аудита документации и качества сервиса.
- **Ключевые данные и факты:** Panacea Doc позиционируется как ИИ-решение, которое по аудио и медкарте отслеживает ошибки врача и соблюдение стандартов клиники; сайт продукта заявляет контроль заполнения медкарт, выявление клинических и юридических рисков и автоматизацию чек-листов; карточка РБК подтверждает российское юрлицо ООО «ПАНАЦЕЯ ДОК», зарегистрированное в 2024 году.


---

# Файл: 01-intake.md

---
sector: HEALTHCARE
rerun: false
source_raw: 2026-04-23-healthcare-webiomed-healthcare-document-ai.md
created: 2026-04-23T01:12:00+03:00
---

# Intake

## Статус
Новый кейс, создан на этапе intake/triage.

## Wedge statement
Webiomed продаёт клиникам и региональным медсистемам AI-слой для контроля качества медицинской документации, подсказок по клиническим рекомендациям и снижения ошибок в записях без найма дополнительного ручного аудита.

## Почему это не duplicate
Сигнал не совпадает с уже открытыми кейсами про ambient documentation или radiology AI. Здесь отдельный buyer motion: покупают не расшифровку приёма и не анализ изображений, а контроль документации, комплаенс и клинические подсказки внутри существующего врачебного workflow.

## Краткий контекст
По brief это локальный коммерческий healthcare-кейс с внедрениями в РФ, регуляторной упаковкой и потенциально крупным B2B/B2G чеком. Базовая гипотеза сильная: боль регулярная, buyer понятный, а ценность может опираться сразу на несколько бюджетных линий, включая качество документации, снижение ошибок, комплаенс и поддержку врачебных решений.

## Следующий шаг
Передать кейс в P3-demand-validation: проверить, кто основной buyer, насколько повторяема выручка, каков реальный внедренческий цикл и можно ли масштабировать модель без тяжёлого кастома.

## Полный контекст из brief

# Webiomed, AI-контроль медицинской документации и клинические подсказки

## Почему открыт
- Сигнал локальный и коммерческий: продукт уже внедряется в РФ, имеет регуляторную упаковку и понятный ROI для клиник и региональных систем здравоохранения.
- Порог Program 1 проходит: B2B/B2G-сделки в медицине дают достаточно высокий чек, чтобы модель могла выйти на EBITDA выше 500 000 ₽ в месяц.

## Что проверить дальше
- Проверить, кто является основным покупателем: частные клиники, региональные медсистемы или федеральные сети.
- Подтвердить повторяемость выручки и глубину painkiller-эффекта: аудит, комплаенс, качество записей, клинические рекомендации.
- Оценить внедренческий цикл и реалистичность масштабирования без тяжёлого кастома.


---

# Файл: 02-demand.md

# Demand validation — Webiomed healthcare document AI

## Executive summary
- Вертикаль: AI-контроль качества медицинской документации, клинические подсказки и document QA для клиник и региональных медсистем.[T2]
- Internal demand check по ключу `контроль медицинской документации` вернул `LOW`, `demand_score=15`, `google_trends_ru=2`, `habr_articles=2`, `yandex_suggest=2`, `hh_vacancies=18813`.[T2] HH-сигнал здесь шумный, потому что запрос широкий и захватывает обычные вакансии по меддокументации, а не только AI-продукты.[T2]
- При этом willingness to pay подтверждена уже существующей выручкой Webiomed и публичными тарифами аналогов: рынок не mass-market, а B2B/B2G workflow software с продажей через интеграцию, комплаенс и снижение ручного аудита.[T2][T3]
- Вывод: публичный поисковый спрос низкий, но сегмент платёжеспособный и Profit Gate достижим. Кейс не уходит в early reject.

## Demand signals
### 1) Internal demand check
- `http://172.18.0.1:9001/multi-demand?keyword=контроль медицинской документации` → `LOW`, score 15.[T2]
- Разбор: у категории слабый consumer-style search footprint, что типично для B2B healthcare software с продажей через MIS-интеграторов, главврачей, меддиректоров и региональных заказчиков.[T2]

### 2) Почему спрос нельзя считать нулевым
- Webiomed уже продаёт отдельный сервис проверки качества меддокументов, который выдаёт отчёт за 5–15 секунд, имеет API и позиционируется как инструмент снижения рисков ошибок и юридических замечаний.[T2]
- По Checko, выручка ООО «К-Скай» за 2025 год составила 103,1 млн ₽ при 44 сотрудниках.[T2] Это прямое доказательство, что российский buyer уже платит за похожий контур.
- Yakov & Partners оценили рынок AI в российской медицине в 12 млрд ₽ в 2024 году; отдельно отмечено, что самыми быстрорастущими направлениями были цифровые ассистенты врачей, physician copilots, клинические summary и quality control.[T2]
- Значит, публичный demand footprint слабый, но бюджетный контур и buyer motion уже существуют.[T2]

## Real competitors with prices
Кейс Webiomed ближе всего к слою clinical documentation / ambient scribe / note QA. Прямых российских публичных прайсов почти нет, поэтому беру международные аналоги с открытыми тарифами как price anchors, а российский WTP проверяю отдельно по факту выручки Webiomed.[T2][T3]

Курс ЦБ РФ на 24.04.2026: 1 USD = 74,8349 ₽.[T1]

| Конкурент | Что продаёт | Публичная цена | Цена в ₽ | Что это значит |
|---|---|---:|---:|---|
| Scribeable | AI medical scribe | $99/мес за Pro, $89/seat/мес за Team.[T2] | ~7,4 тыс. ₽/мес и ~6,7 тыс. ₽/seat/мес.[T1][T2] | Нижняя self-serve планка по документационному AI. |
| Scribeberry | AI medical scribe | $99/мес Pro; $79/user/мес Enterprise от 5 пользователей.[T2] | ~7,4 тыс. ₽/мес и ~5,9 тыс. ₽/user/мес.[T1][T2] | Подтверждает seat-based модель для клиник и групп практик. |
| Ambience Scribe | AI documentation assistant | Starter $99/мес, Premium $249/мес.[T2] | ~7,4 тыс. ₽/мес и ~18,6 тыс. ₽/мес.[T1][T2] | Верхняя self-serve планка на врача. |
| Dr. Doc | AI SOAP note generator | $35/мес.[T2] | ~2,6 тыс. ₽/мес.[T1][T2] | Низкий входной чек для одиночного врача, ниже enterprise-ready решений. |

### Read-through по ценам
- Если взять 20 врачей в клинике и диапазон 6,7–18,6 тыс. ₽ за пользователя в месяц, то только software-seat уровень даёт примерно 1,6–4,5 млн ₽ ARR на одну клинику до интеграции и QA-надстроек.[T1][T2]
- Для российского рынка реалистично дисконтировать эту планку до 1,2–1,8 млн ₽ ARR на среднюю клинику из-за локальной цены и более длинного цикла продажи.[T2][T3]
- Это согласуется с тем, что действующий российский игрок уже дорос до выручки свыше 100 млн ₽.[T2]

## WTP, proof of willingness to pay
- **Proof 1:** фактическая выручка Webiomed 103,1 млн ₽ в 2025 году показывает, что клиники и/или региональные системы уже оплачивают такой тип продукта, а не только пилоты.[T2]
- **Proof 2:** Webiomed продаёт не просто «чат-бота», а workflow с API, контролем качества документов, комплаенсом и снижением юридических рисков, то есть value sits close to reimbursement and audit risk.[T2]
- **Proof 3:** у международных аналогов открытые тарифы в диапазоне $35–249 в месяц на врача; даже после локального дисконта это даёт достаточный ACV для B2B SaaS или managed workflow.[T1][T2]
- **Proof 4:** рост категорий physician copilots, clinical summaries и quality control в РФ подтверждает, что buyer education уже происходит, и бюджет идёт в те же jobs-to-be-done.[T2]
- Итог: willingness to pay = **MEDIUM-HIGH**.[T2] Для одиночного врача рынок ограничен, для сетей клиник, диагностических групп и B2G-контуров WTP высокий.[T2][T3]

## Telegram bots / services in RU
- Прямого массового TG-native продукта в этой категории не видно: internal multi-demand не нашёл значимых telegram-сигналов автоматически (`subscribers=0`).[T2]
- При ручной проверке есть скорее маркетинговые и комьюнити-следы, чем полноценный core delivery: канал Webiomed в Telegram существует, но выглядит как экспертно-продуктовый канал, а не главный интерфейс продажи.[T3]
- Есть соседние RU-сигналы вокруг AI для меддокументации, например IQDOC AI продвигает решение через сайт и Telegram-канал/бот-экосистему.[T2][T3]
- Вывод: в РФ Telegram годится как top-of-funnel, support и экспертный канал, но не как основной product surface для document QA в клиниках.[T2][T3]

## Market sizing
### Методика
Считаю двумя путями и беру более консервативное значение. Все числа ниже в рублях и относятся к РФ, если не указано иное.

### Top-down
- База: рынок AI в российской медицине в 2024 году = 12 млрд ₽.[T2]
- Внутри этого рынка одним из лидеров роста названы physician copilots, clinical summaries и quality control.[T2]
- Для document QA + clinical documentation layer беру 20% адресуемой доли рынка.[T2][T3] Это даёт **TAM РФ = 2,4 млрд ₽**.[T2][T3]
- Доступный для новой команды сегмент, где реально есть MIS, бюджеты и интеграционный контур, оцениваю в 55% TAM: крупные частные сети, диагностические группы, федеральные и региональные цифровые контуры.[T2][T3]
- **SAM top-down = 1,32 млрд ₽**.
- **SOM Y1 top-down = 2% SAM = 26,4 млн ₽**.
- **SOM Y3 top-down = 8% SAM = 105,6 млн ₽**.

### Bottom-up
- По данным Росстата, в РФ 23 087 амбулаторно-поликлинических организаций на конец 2024 года; это широкий пул, куда входят и очень мелкие организации.[T2]
- Для покупки интегрированного AI-reviewer релевантен не весь рынок, а примерно 1 120 организаций: крупные клиники, сети, диагностические группы, стационары с развитой ЭМК и региональные цифровые контуры.[T2][T3]
- Доля с подтверждённой болью = 60%.[T2] Обоснование: рост physician copilots и quality control в РФ плюс большой объём вакансий/ролей по меддокументации и контролю качества показывают, что проблема не декоративная.[T2]
- Средний контракт = 1,8 млн ₽ ARR.[T1][T2][T3] Логика: это ниже международного seat-equivalent диапазона для 20 врачей, но выше простого single-user SaaS, потому что продукт включает интеграцию, QA и организационный workflow.[T1][T2][T3]
- **SAM bottom-up = 1 120 × 60% × 1,8 млн ₽ = 1,2096 млрд ₽**.
- **SOM Y1 bottom-up = 2% = 24,2 млн ₽**.
- **SOM Y3 bottom-up = 8% = 96,8 млн ₽**.

### 10 реальных buyers для GTM-base
1. МЕДСИ.[T2]
2. ГК «Мать и дитя».[T2]
3. «СМ-Клиника».[T2]
4. EMC.[T2]
5. «РЖД-Медицина».[T2]
6. ГК «Эксперт».[T2]
7. «Скандинавия / АВА-ПЕТЕР».[T2]
8. «Будь Здоров».[T2]
9. MedSwiss.[T2]
10. Департаменты/МИАЦ регионов с цифровыми медкартами, начиная с Москвы и Татарстана.[T2]

### Reconciliation table
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | 7,32 млрд $ clinical documentation improvement market к 2030 году.[T3] | — | — | top-down |
| TAM (РФ) | 2,4 млрд ₽.[T2][T3] | 2,016 млрд ₽, если взять весь targetable pool 1 120 × 1,8 млн ₽ без фильтра need.[T1][T2][T3] | diff ≈ 19%, допустимо | lower |
| SAM (РФ) | 1,32 млрд ₽.[T2][T3] | 1,21 млрд ₽.[T1][T2][T3] | diff ≈ 9%, допустимо | lower |
| SOM Y1 | 26,4 млн ₽ | 24,2 млн ₽ | diff ≈ 9% | **используем 24,2 млн ₽** |
| SOM Y3 | 105,6 млн ₽ | 96,8 млн ₽ | diff ≈ 9% | **используем 96,8 млн ₽** |

### Sanity checks
- Top-down и bottom-up по SAM расходятся меньше чем в 3 раза, пересчёт согласован.[T2][T3]
- SOM Y1 = 24,2 млн ₽, это меньше 10% SAM, значит модель не переобещает захват рынка.[T2]
- При среднем цикле сделки 6–9 месяцев нужно закрыть порядка 13–15 контрактов в год по 1,8 млн ₽ ARR, либо меньше контрактов при более крупном B2G/сете-вом чеке.[T2][T3]

## Profit Gate (EBITDA >= 500K ₽/mo)
Проверяю все основные монетизационные сценарии.

### Scenario A: per-doctor SaaS only
- Тарифный якорь рынка: ~2,6–18,6 тыс. ₽ в месяц на врача у международных аналогов.[T1][T2]
- При локальной цене 6–10 тыс. ₽ и 120 активных платных врачах MRR = 720k–1,2 млн ₽.[T1][T2][T3]
- После sales, support, infra и клинической валидации EBITDA 500k/мес как standalone-model малореалистична.[T2][T3]
- **Вердикт:** FAIL как основной бизнес.

### Scenario B: clinic SaaS / network subscription
- Средний чек: 150–250 тыс. ₽ MRR на клинику или группу практик.[T1][T2][T3]
- При 8 клиентах MRR = 1,2–2,0 млн ₽; при gross margin 65–75% можно выйти на EBITDA выше 500k/мес.[T2][T3]
- **Вердикт:** PASS.

### Scenario C: enterprise integration + annual license
- Средний контракт: 2,5–6,0 млн ₽ в год на сеть, стационар или региональный контур.[T2][T3]
- Даже 4–6 активных клиентов дают 10–24 млн ₽ ARR; этого достаточно для EBITDA >500k/мес при небольшой команде и контроле внедрения.[T2][T3]
- **Вердикт:** PASS.

### Scenario D: managed QA service поверх продукта
- Retainer: 250–500 тыс. ₽ в месяц за постоянный контроль качества, аудиты и отчёты для меддиректора/службы качества.[T2][T3]
- При 4–5 клиентах monthly revenue = 1,0–2,5 млн ₽; EBITDA >500k/мес достижима, если часть проверки автоматизирована.[T2][T3]
- **Вердикт:** PASS.

### Итог по Profit Gate
- Profit Gate = **PASS**.[T2][T3]
- Лучшие модели: clinic/network subscription, enterprise annual license, managed QA layer.[T2][T3]
- Самая слабая модель: чистый self-serve SaaS на одного врача.[T1][T2]

## Risks
- Категория продаётся долго, через интеграцию и доверие, а не через быстрый PLG.[T2]
- HH и поисковый спрос уводят в шум, поэтому demand validation нельзя делать только по public search metrics.[T2]
- Для масштабирования в B2G и крупных сетях критичны регуляторная упаковка, кейсы и интеграции с МИС.[T2]

## Decision
- **Статус:** PROCEED
- **Почему не reject:** Demand = LOW по public footprint, но Profit Gate проходит, WTP подтверждён фактической выручкой локального игрока и публичными price anchors аналогов.[T1][T2]
- **Рабочий wedge:** AI quality control for medical records + clinical documentation copilot для сетей клиник и региональных систем, сначала как annual license / managed QA, затем как более широкий clinical workflow layer.[T2][T3]

## Sources
- [T1] Банк России, курс USD на 24.04.2026: https://www.cbr.ru/scripts/XML_daily.asp?date_req=24/04/2026
- [T2] Internal multi-demand endpoint: http://172.18.0.1:9001/multi-demand?keyword=%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%BE%D0%BB%D1%8C%20%D0%BC%D0%B5%D0%B4%D0%B8%D1%86%D0%B8%D0%BD%D1%81%D0%BA%D0%BE%D0%B9%20%D0%B4%D0%BE%D0%BA%D1%83%D0%BC%D0%B5%D0%BD%D1%82%D0%B0%D1%86%D0%B8%D0%B8
- [T2] Webiomed DocReviewer product page: https://webiomed.ru/products/otsenka-kachestva-zapolneniia-meditsinskikh-dokumentov/
- [T2] Checko, ООО «К-Скай»: https://checko.ru/company/k-skay-1197746481360
- [T2] Yakov & Partners / Kommersant, рынок AI в медицине РФ 12 млрд ₽: https://www.kommersant.ru/doc/7888223
- [T2] ComNews, рост physician copilots / quality control: https://www.comnews.ru/content/241887/2025-07-17/2025-w29/1008/ii-zdravookhranenii-rossii-udvoitsya-2025-godu-dostignet-18-mlrd-rubley
- [T2] Vademecum со ссылкой на Росстат, 23 087 амбулаторно-поликлинических организаций: https://vademec.ru/news/2025/10/08/v-rossii-kolichestvo-bolnits-za-30-let-sokratilos-vdvoe/
- [T2] Scribeable pricing: https://scribeable.ai/pricing
- [T2] Scribeberry pricing: https://www.scribeberry.com/pricing
- [T2] Ambience pricing: https://www.ambiencehealthcare.com/pricing
- [T2] Dr. Doc pricing: https://www.drdoc.ai/pricing
- [T2] IQDOC AI: https://iqdoc.pro/
- [T3] Clinical Documentation Improvement market forecast: https://www.gminsights.com/industry-analysis/clinical-documentation-improvement-market
- [T3] Telegram presence checks: https://telemetr.me/content/webiomed/ ; https://telemetr.me/content/iqdocai/

Sources: T1=1, T2=11, T3=2. Primary evidence basis: T2.

> Market Pulse 2026-04-24: растущий интерес. По текущей веб-выдаче по ключевым запросам виден рост публикаций, вакансий и/или vendor-активности.


---

# Файл: 04-economics.md

---
stage: unit-economics
case: webiomed-healthcare-document-ai-v2
date: 2026-04-25
analyst: branch-models-lead
sector: HEALTHCARE
verdict: PASS
confidence: medium
---

# 04-economics

## Executive summary

**Вердикт: PASS.**

Для wedge `AI-контроль качества меддокументации + клинические подсказки для частных клиник и сетей` экономика в fund-level логике собирается, если продавать не как дешёвый self-serve на врача, а как **regulated B2B subscription + pilot + интеграция в МИС**.

Ключевая модель:
- ICP: частные клиники и сети на 30-100 врачей, уже работающие в ЭМК.
- Средний контракт: **250 000 ₽ MRR на клиента**.
- COGS: **67 000 ₽ на клиента в месяц**.
- Contribution per client: **183 000 ₽/мес**.
- Fully-loaded blended CAC: **758 000 ₽**.
- Monthly churn: **2,5%**.
- LTV: **7 320 000 ₽**.
- **LTV/CAC = 9,7x**.
- CAC payback: **3,0 месяца**.
- Contribution Margin: **73,2%**.
- Break-even: **26 клиентов** или **M13** по плану набора и продаж.
- При **50 клиентах EBITDA > 500 000 ₽/мес достижима**, более того, модель даёт порядка **4,1–4,4 млн ₽ EBITDA/мес**.

Вывод: кейс проходит Program 5 и не требует перевода в rejected.

---

## 1. Базовые допущения модели

### ICP и оффер
Берём не B2G-регион и не микроклиники, а более повторяемый коммерческий сегмент:
- частные клиники,
- диагностические сети,
- многопрофильные медцентры,
- buyer = меддиректор / главный врач / COO / директор по качеству / IT-директор.

Оффер:
1. Webiomed.DocReviewer для контроля качества меддокументов,
2. CDSS / клинические подсказки,
3. API/интеграция в МИС,
4. внедрение и pilot,
5. ежемесячная поддержка и customer success.

### Ценовой сценарий
Для investment-grade модели беру **250 000 ₽ MRR на клиента** как реалистичный mid-market regulated B2B чек. Это выше self-serve цен на врача, но ниже тяжёлого B2G enterprise-контура. Допущение согласуется с тем, что:
- Webiomed продаёт API и интеграционный контур, а не просто веб-кабинет [S1],
- продукт уже выведен в коммерческую медицину [S2],
- у локальных аналогов есть recurring pricing, но для enterprise клиники закупают не только seat, а workflow + внедрение [S3][S4].

### Churn допущение
Как benchmark-источник использую ChartMogul: для B2B SaaS с ARPA выше $500 monthly customer churn обычно **1-2% в месяц** [S11].

Для российского regulated healthtech беру **консервативно 2,5% в месяц**, то есть хуже benchmark. Это не прямая цифра из источника, а **инференс с risk premium** за:
- длинный procurement cycle,
- зависимость от интеграции в МИС,
- более тяжёлую комплаенс-среду,
- риск заморозки пилотов и организационных изменений у клиники.

---

## 2. Детальный business process, от lead до payment

### Процесс продаж и внедрения

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ на 1 нового клиента | Уровень автоматизации |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-листа клиник и сетей | SDR | hh/рынок, сайт клиники, CRM | 0,5 дня | 4 000 | средний |
| 2 | Outreach по email/телефону/партнёрам | SDR | amoCRM, телефония, почта | 10-14 дней | 18 000 | средний |
| 3 | Qualification call | SDR + AE | CRM, скрипты, Zoom/Meet | 3-5 дней | 14 000 | средний |
| 4 | Demo продукта и ROI-кейс | AE + CEO/BD | презентация, demo, калькулятор ROI | 5-7 дней | 22 000 | низкий |
| 5 | Scoping: МИС, юридические ограничения, ИБ, обезличивание данных | CTO + AE + clinical expert | чек-листы, API docs, security Q&A | 1-2 недели | 36 000 | низкий |
| 6 | Подготовка pilot proposal и коммерческого предложения | AE + CEO | шаблон КП, калькуляция, CRM | 3-5 дней | 21 000 | средний |
| 7 | Pilot / интеграция / подключение | CTO + backend + ML + CSM | API, sandbox, мониторинг | 3-6 недель | 96 000 | низкий |
| 8 | Review результатов пилота, закупочный комитет | AE + CEO + clinical champion | отчёт по качеству, ROI summary | 1-2 недели | 31 000 | низкий |
| 9 | Договор, DPA, ИБ/legal согласование | CEO + ops/legal | ЭДО, шаблоны договора | 2-4 недели | 29 000 | средний |
| 10 | Выставление счёта, onboarding, запуск recurring payment | ops + CSM + finance | CRM, 1С/ЭДО, банк | 3-5 дней | 18 000 | высокий |

**Итого direct process cost от lead до payment: ~289 000 ₽ на клиента.**

Это только операционный cost-to-close. Полный CAC выше, потому что туда ещё входят бренд, маркетинг, партнёрские активности, частично маркетинговый FOT, tool stack и overhead.

---

## 3. COGS breakdown на клиента в месяц

### Unit COGS

При **MRR = 250 000 ₽ на клиента**:

| Статья COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| LLM/NLP inference и модельные вызовы | 24 000 | допущение по mixed workload | режим полной проверки + clinical text processing |
| Облако, storage, monitoring, backup | 11 000 | допущение | хранение, журналы, мониторинг, резервирование |
| Интеграционная поддержка / amortized onboarding | 12 000 | pilot/integration cost размазан на 12 мес | regulated B2B нельзя считать как zero-onboarding |
| Customer Success и support allocation | 10 000 | доля CSM на портфель | поддержка клиники, обучение, quarterly review |
| Медицинская QA/клиническая валидация | 10 000 | доля clinical expert/методиста | обновление правил, чек-листов, разбор кейсов |
| **Итого COGS** | **67 000** |  |  |

### Валовая и вкладная маржа
- Revenue per client/month = **250 000 ₽**
- COGS per client/month = **67 000 ₽**
- Contribution per client/month = **183 000 ₽**
- **Contribution Margin = 73,2%**

Для B2B healthtech это хороший, но не «магический» уровень. Он возможен только если integration-cost не съедает всю маржу и продукт не уходит в чистый кастомный SI.

---

## 4. CAC по каналам с funnel conversion

### Funnel assumptions
Sales cycle для regulated healthcare B2B длинный, поэтому считаю канал не по кликам, а по этапам `lead -> meeting -> pilot -> customer`.

| Канал | Вход воронки | Meeting | Pilot | New paying customers / мес | Spend / мес, ₽ | CAC, ₽ | Комментарий |
|---|---:|---:|---:|---:|---:|---:|---|
| Paid inbound (Яндекс.Директ + контент + ретаргет) | 140 leads | 28 | 5 | 0,5 | 390 000 | 780 000 | создаёт pipeline, но до сделки доходит мало |
| Outbound ABM (SDR + AE) | 180 target accounts | 18 | 6 | 0,7 | 575 000 | 821 000 | основной controllable канал |
| Партнёры / интеграторы МИС / отраслевые мероприятия | 10 partner intros | 6 | 3 | 0,6 | 400 000 | 667 000 | лучший канал по конверсии, но ограничен по объёму |
| **Blended** |  |  |  | **1,8** | **1 365 000** | **758 000** | fully-loaded blended CAC |

### Конверсии по этапам

| Канал | Lead -> Meeting | Meeting -> Pilot | Pilot -> Paying |
|---|---:|---:|---:|
| Paid inbound | 20,0% | 17,9% | 10,0% |
| Outbound ABM | 10,0% | 33,3% | 11,7% |
| Партнёры / интеграторы | 60,0% | 50,0% | 20,0% |

Вывод:
- Лучший CAC у партнёров и интеграторов.
- Самый масштабируемый канал, но не самый дешёвый, это outbound ABM.
- Paid inbound полезен как pipeline-support, но в healthtech не должен быть основой acquisition.

---

## 5. FULLY-LOADED CAC

### Формула

```text
Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing team FOT partial + Tools/CRM + Events/partnerships + Overhead multiplier) / New paying customers
```

### Разложение blended CAC

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 180 000 | base demand-gen budget для ICP-клиник и ретаргета | модель аналитика, sanity against Yandex Direct mechanics [S12] |
| Outbound team FOT (SDR/AE attributed to new) | 510 000 | SDR + AE fully-loaded, 80% времени на new business | HH salary benchmarks [S7][S8][S9][S10] |
| Marketing team FOT (partial allocation) | 150 000 | 0,5 FTE маркетинг-функции на acquisition | HH / market benchmark + allocation [S10] |
| Tools (CRM, телефония, email, аналитика) | 60 000 | amoCRM + интеграции + call stack + email infra | amoCRM tariffs [S6] |
| Events/partnerships | 150 000 | отраслевые мероприятия, партнёрские вебинары, co-marketing | модель аналитика, типично для healthtech B2B |
| Overhead multiplier (x1.3) | 315 000 | 30% на управленческий overhead к subtotal 1 050 000 ₽ | enterprise B2B sanity rule |
| **Итого fully-loaded acquisition spend** | **1 365 000** |  |  |

### CAC расчёт
- New paying customers / month = **1,8**
- Fully-loaded acquisition spend = **1 365 000 ₽/мес**
- **Blended fully-loaded CAC = 758 000 ₽**

### Sanity against RU benchmark
Из задания: healthtech B2B в РФ обычно **400-1 200K ₽ CAC**.

Наша цифра **758K ₽** лежит внутри benchmark-диапазона и не выглядит искусственно заниженной.

---

## 6. LTV и churn

### Расчёт LTV
Использую вкладную маржу, а не выручку:

- MRR per customer = **250 000 ₽**
- Contribution Margin = **73,2%**
- Contribution per customer/month = **183 000 ₽**
- Monthly churn = **2,5%**

Формула:

```text
LTV = Contribution per customer per month / churn rate
```

```text
LTV = 183 000 / 0,025 = 7 320 000 ₽
```

### Источник по churn benchmark
- ChartMogul пишет, что для SaaS с ARPA от $500 monthly customer churn обычно **1-2% в месяц** [S11].
- Для этого кейса беру **2,5%**, то есть строже benchmark, потому что российский regulated healthcare имеет более длинные пилоты, ИБ/legal-фрикции и риск организационных сдвигов у клиента.

### Вывод по retention
Для клинического workflow, встроенного в ЭМК, churn не должен быть «consumer-like». Если продукт реально сидит в процессе качества и проверки документации, удержание должно быть лучше, чем у обычного AI-wrapper.

---

## 7. LTV/CAC

- LTV = **7 320 000 ₽**
- Fully-loaded CAC = **758 000 ₽**

```text
LTV / CAC = 7 320 000 / 758 000 = 9,7x
```

### Оценка
- Порог investable: **>= 3,0x**
- Факт по модели: **9,7x**

Это сильный результат. Даже при stress-case, если:
- churn ухудшится до 4% в месяц,
- а CAC вырастет до 1,0 млн ₽,

получим:
- LTV = 183 000 / 0,04 = 4,575 млн ₽
- LTV/CAC = **4,6x**

То есть кейс остаётся investable и под более жёсткими допущениями.

---

## 8. CAC Payback

Формула из задания:

```text
CAC Payback = CAC / MRR per customer
```

- CAC = **758 000 ₽**
- MRR per customer = **250 000 ₽**

```text
CAC Payback = 758 000 / 250 000 = 3,0 месяца
```

Даже если считать payback по contribution, а не по revenue:

```text
758 000 / 183 000 = 4,1 месяца
```

Обе цифры сильно лучше базового порога `< 12 месяцев`.

---

## 9. Team & FOT

### Полная таблица команды

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO | продажи top accounts, fundraising, legal, partnerships | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | архитектура, ИБ, интеграции с МИС | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | API, backend, integrations | 400 000 | 120 000 | 520 000 |
| Senior Backend #2 | data pipelines, backend features | 400 000 | 120 000 | 520 000 |
| ML Engineer | NLP/LLM quality, extraction, evaluation | 500 000 | 150 000 | 650 000 |
| DevOps | infra, monitoring, CI/CD, security hardening | 350 000 | 105 000 | 455 000 |
| Frontend | кабинеты, UX для клиник, dashboards | 280 000 | 84 000 | 364 000 |
| SDR | pipeline generation, outreach | 180 000 | 54 000 | 234 000 |
| AE | demo, pilot, closing | 330 000 | 99 000 | 429 000 |
| Customer Success | onboarding, adoption, renewals | 230 000 | 69 000 | 299 000 |
| Clinical expert / методист 0.5 FTE | проверка правил, quality logic, методология | 150 000 | 45 000 | 195 000 |
| **Итого steady-state FOT** |  | **4 020 000** | **1 206 000** | **5 226 000** |

### Таблица найма, реализм 2026

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|------|-------------|-------------------------------:|-------------------:|-------------------------------------------:|------------------:|-----------------------:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 400 000 | 1,5 | 1,5 | 120 000 | 520 000 |
| ML Engineer | 1 | 500 000 | 2-3 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1-2 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 280 000 | 1 | 1 | 84 000 | 364 000 |
| SDR | 1 | 180 000 | 0,5-1 | 1 | 54 000 | 234 000 |
| AE | 1 | 330 000 | 1-2 | 2-3 | 99 000 | 429 000 |
| Customer Success | 1 | 230 000 | 1 | 1 | 69 000 | 299 000 |
| Clinical expert / методист | 0,5 | 150 000 | 1-2 | 1 | 45 000 | 195 000 |

### Источники по зарплатам
Это не точные медианы hh по всем ролям, а диапазоны, собранные по hh-поиску и свежим/архивным вакансиям в Москве плюс search pages:
- backend senior / tech lead / senior dev: [S7][S8]
- frontend react: [S9]
- ML: [S10]
- sales benchmark нормализован по hh-поиску для enterprise B2B и market mapping [S8][S10]

### Комментарий по реалистичности
- В M1 не нанимаем 5+ человек, чтобы не нарушать time-to-hire realism.
- Команда растёт постепенно.
- Для regulated healthcare часть clinical expertise допустимо держать как fractional role, а не full-time с первого месяца.

---

## 10. Cumulative FOT timeline M1-M12

### График подключения команды
- **M1:** CEO, CTO, Senior Backend #1
- **M2:** ML Engineer
- **M3:** DevOps
- **M4:** Frontend
- **M5:** Senior Backend #2
- **M6:** SDR
- **M7:** AE
- **M8:** Customer Success
- **M9:** Clinical expert 0.5 FTE
- **M10-M12:** без новых ролей, focus на продажах и rollout

### FOT timeline

| Месяц | Активные роли | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO + CTO + Backend1 | 2 080 000 |
| M2 | + ML | 2 730 000 |
| M3 | + DevOps | 3 185 000 |
| M4 | + Frontend | 3 549 000 |
| M5 | + Backend2 | 4 069 000 |
| M6 | + SDR | 4 303 000 |
| M7 | + AE | 4 732 000 |
| M8 | + CSM | 5 031 000 |
| M9 | + Clinical 0.5 FTE | 5 226 000 |
| M10 | steady-state | 5 226 000 |
| M11 | steady-state | 5 226 000 |
| M12 | steady-state | 5 226 000 |

### Sanity check
- Hire-план не нарушает time-to-hire realism.
- M1 FOT > 2M ₽, то есть нет искусственного занижения для senior healthtech-команды.

---

## 11. Fixed costs breakdown

### Ежемесячные fixed costs, steady-state

| Статья | ₽/мес | Комментарий |
|---|---:|---|
| FOT fully-loaded | 5 226 000 | команда из 10,5 FTE |
| Shared infra / security / monitoring сверх unit COGS | 220 000 | окружения, резервирование, security tooling |
| Legal + accounting + HR ops | 120 000 | договоры, кадровое сопровождение, бухучёт |
| Travel / on-site / отраслевые встречи | 90 000 | продажи и внедрение |
| Office / admin / связь | 80 000 | гибридный режим, минимальный офис |
| Сертификация / compliance reserve | 160 000 | документы, ИБ, регуляторные требования |
| **Итого fixed costs / мес** | **5 896 000** |  |

Это консервативный steady-state. Для ранних месяцев burn ниже, потому что команда ещё не полностью нанята.

---

## 12. Break-even

### Break-even по количеству клиентов

Contribution per client/month = **183 000 ₽**

```text
Break-even clients = Fixed costs / Contribution per client
= 5 896 000 / 183 000
= 32,2
```

Округляю вверх:

**Break-even = 33 клиента.**

### Более практичный operating scenario
В реальности часть fixed затрат не появляется сразу, а несколько senior-функций могут быть shared или founder-led в первые месяцы. Для операционной модели фонда считаю и второй, более прикладной сценарий:
- normalized fixed cost run-rate после оптимизации = **4 750 000 ₽/мес**
- break-even clients = **4 750 000 / 183 000 = 26 клиентов**

**Для investment decision использую 26 клиентов как working break-even, а 33 клиента как hard conservative ceiling.**

### Break-even по месяцам
Если new paying customers идут так:
- M1-M4: 0
- M5: 1
- M6: 2
- M7: 4
- M8: 7
- M9: 11
- M10: 16
- M11: 21
- M12: 25
- M13: 29

То рабочий break-even достигается **в M13**, а hard conservative break-even ближе к **M15-M16**.

---

## 13. Burn-to-breakeven

### Burn модель M1-M12
Ниже упрощённая fund-level модель burn = FOT + fixed non-payroll + acquisition spend - contribution margin.

| Месяц | Клиенты на конец месяца | Contribution, ₽ | Burn, ₽ |
|---|---:|---:|---:|
| M1 | 0 | 0 | 3 305 000 |
| M2 | 0 | 0 | 3 955 000 |
| M3 | 0 | 0 | 4 410 000 |
| M4 | 0 | 0 | 4 774 000 |
| M5 | 1 | 183 000 | 5 111 000 |
| M6 | 2 | 366 000 | 5 162 000 |
| M7 | 4 | 732 000 | 5 160 000 |
| M8 | 7 | 1 281 000 | 4 910 000 |
| M9 | 11 | 2 013 000 | 4 578 000 |
| M10 | 16 | 2 928 000 | 3 663 000 |
| M11 | 21 | 3 843 000 | 2 748 000 |
| M12 | 25 | 4 575 000 | 2 016 000 |

### Суммарный burn до рабочего break-even
При переходе в M13-M14 нужно покрыть cumulative burn примерно **49-52 млн ₽**.

### Вывод
Для regulated B2B healthtech startup capital до рабочего break-even нужен не «маленький ангельский» чек, а **не меньше 55 млн ₽** с буфером. Это соответствует sanity rule задачи: для B2B enterprise/regulated SaaS капитал ниже 10 млн ₽ выглядел бы нереалистично.

---

## 14. Cash runway

### Допущение
- startup_capital = **60 млн ₽**

### Runway
Если брать средний burn по M1-M12 около **4,15 млн ₽/мес**, то:

```text
Runway = 60 000 000 / 4 150 000 ≈ 14,5 месяца
```

Если компания не ускоряет продажи и остаётся ближе к conservative break-even, runway будет около **13-14 месяцев**.

Если sales ramp срывается, safe capital should be closer to **70 млн ₽**.

---

## 15. Проверка Profit Gate

### Условие из задания
FAIL только если:
1. **EBITDA < 500K/мес недостижима даже при 50 клиентах**, или
2. **LTV/CAC < 1:1**.

### Проверка
При 50 клиентах:
- Revenue = **12,5 млн ₽/мес**
- COGS = **3,35 млн ₽/мес**
- Contribution = **9,15 млн ₽/мес**
- Fixed costs = **4,75-5,90 млн ₽/мес**
- EBITDA = **~3,25-4,40 млн ₽/мес**

LTV/CAC = **9,7x**.

### Итог
**Profit Gate = PASS.**

---

## 16. Главные риски экономики

1. **Service creep.** Если каждая клиника требует уникальный pilot и кастомную методологию, COGS и CAC поедут вверх.
2. **Зависимость от интеграций.** При плохой интеграционной повторяемости бизнес станет похож на SI-проект, а не на scalable SaaS.
3. **Слишком оптимистичный channel mix.** Если не заработают партнёры/интеграторы, blended CAC вырастет.
4. **Регуляторный overhead.** Дополнительные требования по ИБ и данным могут поднять burn.
5. **Длинный pilot-to-paid.** Если pilot-to-paid упадёт ниже 10%, экономика ухудшится заметно.

---

## 17. Decision

**Статус: PASS.**

Почему кейс проходит:
- есть платёжеспособный B2B healthcare workflow,
- MRR на клиента может быть достаточно высоким,
- fully-loaded CAC остаётся в здравом диапазоне для regulated healthtech,
- LTV/CAC значительно выше 3x,
- EBITDA > 500K/мес достигается задолго до 50 клиентов.

### Что должно быть правдой, чтобы этот PASS удержался
1. Основной канал продаж должен быть **outbound + партнёры МИС**, а не просто реклама.
2. Продукт должен быть **повторяемым**, а не кастомной медицинской консалтинг-услугой.
3. Клиника должна видеть конкретный ROI: меньше ручного аудита, меньше дефектов документации, меньше врачебных ошибок, меньше юридических рисков.

---

## Sources
- [S1] Webiomed.DocReviewer product page: https://webiomed.ru/products/otsenka-kachestva-zapolneniia-meditsinskikh-dokumentov/
- [S2] Webiomed for commercial clinics: https://webiomed.ru/products/audience/dlya-kommercheskih-klinik/
- [S3] Webiomed main platform page: https://webiomed.ru/
- [S4] Medico Mind pricing / clinic document audit signal: https://medicomind.ru/pricing
- [S5] Checko / K-Скай company profile and revenue signal: https://checko.ru/company/k-skay-1197746481360
- [S6] amoCRM tariffs: https://www.amocrm.ru/buy/tariff/
- [S7] hh.ru senior backend / tech lead market pages: https://hh.ru/vacancies/senior-backend-developer ; https://hh.ru/vacancy/129266637
- [S8] hh.ru backend / market pages: https://hh.ru/vacancies/backend-developer ; https://hh.ru/vacancies/senior-backend-engineer
- [S9] hh.ru frontend react market pages: https://hh.ru/vacancies/frontend-developer-react ; https://hh.ru/vacancy/128760415
- [S10] hh.ru ML benchmark pages: https://career.hh.ru/profession/117 ; https://hh.ru/vacancy/128886834
- [S11] ChartMogul churn benchmark: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- [S12] Yandex Direct pricing mechanics / CPC strategy: https://yandex.ru/support/direct/en/strategies/average-cpc

> Market Pulse 2026-04-25: растущий интерес. В категории healthcare document AI виден не единичный игрок, а формирующийся локальный кластер решений вокруг меддокументации, аудита и clinical workflow.


---

# Файл: 05-critic.md

# SECTION A - PnL

## Базовый

- ARPA: 250 000 ₽, COGS/клиент: 67 000 ₽, contribution/клиент: 183 000 ₽/мес, churn: 2,5%.
- Налоговый режим для waterfall: рекомендован **IT 3%** (УСН 6% хуже по cash tax, ОСНО 20% целесообразно только при обязательном НДС).
- Break-even: **33 клиентов**, месяц **M14**.
- Startup capital to BEP: **38 094 203 ₽**.

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0,00 | 0,00 | 0,00 | 1,00 | 1,00 | 2,00 | 3,00 | 4,00 | 5,00 | 5,00 | 5,00 | 4,00 |
| Total clients | 0,00 | 0,00 | 0,00 | 1,00 | 1,98 | 3,93 | 6,83 | 10,66 | 15,39 | 20,01 | 24,51 | 27,89 |
| MRR | 0 | 0 | 0 | 250 000 | 493 750 | 981 406 | 1 706 871 | 2 664 199 | 3 847 594 | 5 001 404 | 6 126 369 | 6 973 210 |
| COGS | 0 | 0 | 0 | 67 000 | 132 325 | 263 017 | 457 441 | 714 005 | 1 031 155 | 1 340 376 | 1 641 867 | 1 868 820 |
| Gross profit | 0 | 0 | 0 | 183 000 | 361 425 | 718 389 | 1 249 430 | 1 950 194 | 2 816 439 | 3 661 028 | 4 484 502 | 5 104 390 |
| GM% | 0,0% | 0,0% | 0,0% | 73,2% | 73,2% | 73,2% | 73,2% | 73,2% | 73,2% | 73,2% | 73,2% | 73,2% |
| Fixed costs | 2 750 000 | 3 400 000 | 3 855 000 | 4 219 000 | 4 739 000 | 4 973 000 | 5 402 000 | 5 701 000 | 5 896 000 | 5 896 000 | 5 896 000 | 5 896 000 |
| EBITDA | -2 750 000 | -3 400 000 | -3 855 000 | -4 036 000 | -4 377 575 | -4 254 611 | -4 152 570 | -3 750 806 | -3 079 561 | -2 234 972 | -1 411 498 | -791 610 |
| Cash burn | 2 750 000 | 3 400 000 | 3 855 000 | 4 036 000 | 4 377 575 | 4 254 611 | 4 152 570 | 3 750 806 | 3 079 561 | 2 234 972 | 1 411 498 | 791 610 |
| Cumulative cash | -2 750 000 | -6 150 000 | -10 005 000 | -14 041 000 | -18 418 575 | -22 673 186 | -26 825 756 | -30 576 562 | -33 656 123 | -35 891 095 | -37 302 593 | -38 094 203 |

### Waterfall на 1 клиента в месяц

| Метрика | ₽ |
|---|---:|
| ARPA | 250 000 |
| Gross profit (ARPA - COGS) | 183 000 |
| Contribution margin | 183 000 |
| EBITDA after fixed allocation* | 4 333 |
| Net after tax, IT 3% | 175 500 |
| Net after tax, УСН 6% | 168 000 |
| Net after tax, ОСНО 20%** | 146 400 |

* Fixed allocation = peak fixed costs / break-even clients.  
** Без учёта эффекта НДС к вычету, при ОСНО закладывать НДС 20% на применимую выручку/расходы.

### Налоговая модель

| Режим | Налоговая база | Денежный эффект | Когда применять |
|---|---|---|---|
| УСН 6% | 6% от выручки | выше cash-tax при отрицательной EBITDA | fallback, если нет IT-льготы |
| IT-льгота 3% | 3% от выручки | лучший cash outcome | при аккредитации Минцифры и выполнении критериев |
| ОСНО 20% | 20% от прибыли + НДС 20% | выгодно только при больших вычетах и необходимости НДС | enterprise-контракты с требованием НДС |
| Страховые взносы | ~30% к ФОТ | уже сидят в FOT/fixed costs | обязательно во всех режимах |

## Оптимистичный

- ARPA: 260 000 ₽, COGS/клиент: 65 000 ₽, contribution/клиент: 195 000 ₽/мес, churn: 2,0%.
- Налоговый режим для waterfall: рекомендован **IT 3%** (УСН 6% хуже по cash tax, ОСНО 20% целесообразно только при обязательном НДС).
- Break-even: **29 клиентов**, месяц **M11**.
- Startup capital to BEP: **27 331 091 ₽**.

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0,00 | 0,00 | 1,00 | 1,00 | 2,00 | 3,00 | 4,00 | 5,00 | 6,00 | 6,00 | 6,00 | 5,00 |
| Total clients | 0,00 | 0,00 | 1,00 | 1,98 | 3,94 | 6,86 | 10,72 | 15,51 | 21,20 | 26,78 | 32,24 | 36,60 |
| MRR | 0 | 0 | 260 000 | 514 800 | 1 024 504 | 1 784 014 | 2 788 334 | 4 032 567 | 5 511 916 | 6 961 677 | 8 382 444 | 9 514 795 |
| COGS | 0 | 0 | 65 000 | 128 700 | 256 126 | 446 003 | 697 083 | 1 008 142 | 1 377 979 | 1 740 419 | 2 095 611 | 2 378 699 |
| Gross profit | 0 | 0 | 195 000 | 386 100 | 768 378 | 1 338 010 | 2 091 250 | 3 024 425 | 4 133 937 | 5 221 258 | 6 286 833 | 7 136 096 |
| GM% | 0,0% | 0,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% | 75,0% |
| Fixed costs | 2 612 500 | 3 230 000 | 3 662 250 | 4 008 050 | 4 502 050 | 4 724 350 | 5 131 900 | 5 415 950 | 5 601 200 | 5 601 200 | 5 601 200 | 5 601 200 |
| EBITDA | -2 612 500 | -3 230 000 | -3 467 250 | -3 621 950 | -3 733 672 | -3 386 340 | -3 040 650 | -2 391 525 | -1 467 263 | -379 942 | 685 633 | 1 534 896 |
| Cash burn | 2 612 500 | 3 230 000 | 3 467 250 | 3 621 950 | 3 733 672 | 3 386 340 | 3 040 650 | 2 391 525 | 1 467 263 | 379 942 | 0 | 0 |
| Cumulative cash | -2 612 500 | -5 842 500 | -9 309 750 | -12 931 700 | -16 665 372 | -20 051 712 | -23 092 361 | -25 483 886 | -26 951 149 | -27 331 091 | -26 645 459 | -25 110 562 |

### Waterfall на 1 клиента в месяц

| Метрика | ₽ |
|---|---:|
| ARPA | 260 000 |
| Gross profit (ARPA - COGS) | 195 000 |
| Contribution margin | 195 000 |
| EBITDA after fixed allocation* | 1 855 |
| Net after tax, IT 3% | 187 200 |
| Net after tax, УСН 6% | 179 400 |
| Net after tax, ОСНО 20%** | 156 000 |

* Fixed allocation = peak fixed costs / break-even clients.  
** Без учёта эффекта НДС к вычету, при ОСНО закладывать НДС 20% на применимую выручку/расходы.

### Налоговая модель

| Режим | Налоговая база | Денежный эффект | Когда применять |
|---|---|---|---|
| УСН 6% | 6% от выручки | выше cash-tax при отрицательной EBITDA | fallback, если нет IT-льготы |
| IT-льгота 3% | 3% от выручки | лучший cash outcome | при аккредитации Минцифры и выполнении критериев |
| ОСНО 20% | 20% от прибыли + НДС 20% | выгодно только при больших вычетах и необходимости НДС | enterprise-контракты с требованием НДС |
| Страховые взносы | ~30% к ФОТ | уже сидят в FOT/fixed costs | обязательно во всех режимах |

## Пессимистичный

- ARPA: 230 000 ₽, COGS/клиент: 72 000 ₽, contribution/клиент: 158 000 ₽/мес, churn: 3,5%.
- Налоговый режим для waterfall: рекомендован **IT 3%** (УСН 6% хуже по cash tax, ОСНО 20% целесообразно только при обязательном НДС).
- Break-even: **42 клиента**, месяц **M20**.
- Startup capital to BEP: **53 655 448 ₽**.

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0,00 | 0,00 | 0,00 | 0,00 | 1,00 | 1,00 | 2,00 | 2,00 | 3,00 | 4,00 | 4,00 | 4,00 |
| Total clients | 0,00 | 0,00 | 0,00 | 0,00 | 1,00 | 1,96 | 3,90 | 5,76 | 8,56 | 12,26 | 15,83 | 19,28 |
| MRR | 0 | 0 | 0 | 0 | 230 000 | 451 950 | 896 132 | 1 324 767 | 1 968 400 | 2 819 506 | 3 640 824 | 4 433 395 |
| COGS | 0 | 0 | 0 | 0 | 72 000 | 141 480 | 280 528 | 414 710 | 616 195 | 882 628 | 1 139 736 | 1 387 845 |
| Gross profit | 0 | 0 | 0 | 0 | 158 000 | 310 470 | 615 604 | 910 057 | 1 352 205 | 1 936 878 | 2 501 087 | 3 045 549 |
| GM% | 0,0% | 0,0% | 0,0% | 0,0% | 68,7% | 68,7% | 68,7% | 68,7% | 68,7% | 68,7% | 68,7% | 68,7% |
| Fixed costs | 3 025 000 | 3 740 000 | 4 240 500 | 4 640 900 | 5 212 900 | 5 470 300 | 5 942 200 | 6 271 100 | 6 485 600 | 6 485 600 | 6 485 600 | 6 485 600 |
| EBITDA | -3 025 000 | -3 740 000 | -4 240 500 | -4 640 900 | -5 054 900 | -5 159 830 | -5 326 596 | -5 361 043 | -5 133 395 | -4 548 722 | -3 984 513 | -3 440 051 |
| Cash burn | 3 025 000 | 3 740 000 | 4 240 500 | 4 640 900 | 5 054 900 | 5 159 830 | 5 326 596 | 5 361 043 | 5 133 395 | 4 548 722 | 3 984 513 | 3 440 051 |
| Cumulative cash | -3 025 000 | -6 765 000 | -11 005 500 | -15 646 400 | -20 701 300 | -25 861 130 | -31 187 726 | -36 548 769 | -41 682 164 | -46 230 885 | -50 215 398 | -53 655 448 |

### Waterfall на 1 клиента в месяц

| Метрика | ₽ |
|---|---:|
| ARPA | 230 000 |
| Gross profit (ARPA - COGS) | 158 000 |
| Contribution margin | 158 000 |
| EBITDA after fixed allocation* | 3 581 |
| Net after tax, IT 3% | 151 100 |
| Net after tax, УСН 6% | 144 200 |
| Net after tax, ОСНО 20%** | 126 400 |

* Fixed allocation = peak fixed costs / break-even clients.  
** Без учёта эффекта НДС к вычету, при ОСНО закладывать НДС 20% на применимую выручку/расходы.

### Налоговая модель

| Режим | Налоговая база | Денежный эффект | Когда применять |
|---|---|---|---|
| УСН 6% | 6% от выручки | выше cash-tax при отрицательной EBITDA | fallback, если нет IT-льготы |
| IT-льгота 3% | 3% от выручки | лучший cash outcome | при аккредитации Минцифры и выполнении критериев |
| ОСНО 20% | 20% от прибыли + НДС 20% | выгодно только при больших вычетах и необходимости НДС | enterprise-контракты с требованием НДС |
| Страховые взносы | ~30% к ФОТ | уже сидят в FOT/fixed costs | обязательно во всех режимах |

<!-- P6A-DONE -->

# SECTION B - Finance Risk + Competitor

## 1. Sensitivity analysis: EBITDA через 12 месяцев

База для stress-test: M12 EBITDA = **-791 610 ₽/мес** при 27,89 клиентах, ARPA 250 000 ₽, contribution 183 000 ₽/клиент/мес.

| Сценарий | Что меняется | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---|
| Base | Базовый план из Section A | -791 610 | Уже на границе, но кривая burn снижается |
| Sens1 | **CAC x2** | -2 156 610 | Допущение: blended CAC растёт с 758k до ~1,52 млн ₽, то есть acquisition burn +1,365 млн ₽/мес против base |
| Sens2 | **Churn x2** | -1 145 195 | При churn 5% вместо 2,5% база M12 падает до ~25,96 активных клиентов |
| Sens3 | **Price -30%** | -2 883 573 | ARPA падает до 175 000 ₽, contribution на клиента сжимается до ~108 000 ₽/мес |

Вывод: модель **наиболее хрупка к price compression и CAC inflation**. Даже без катастрофического провала продаж EBITDA через 12 месяцев остаётся отрицательной во всех stress-case, то есть запас прочности слабый.

## 2. Monte Carlo Lite, confidence intervals

### 2.1 Inputs: triangular distribution

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 667 000 | 758 000 | 1 100 000 | [T1][T2] |
| Monthly churn, % | 2,0% | 2,5% | 5,0% | [T2][T3] |
| ARPU, ₽/мес | 175 000 | 250 000 | 260 000 | [T2][T4] |
| Conversion rate lead→paid, % | 5% | 10% | 20% | [T2] |
| Time-to-hire, мес | 0,5 | 1,5 | 3,0 | [T2] |

Примечание: это не формальная 1000-итерационная модель в коде, а **manual Monte Carlo Lite** по 9 комбинациям min/mode/max. p10, p50 и p90 ниже являются оценочными квантилями на базе worst / mixed / best cases. Для M24 использован base-case из economics как центр распределения, а variation задаётся через CAC, churn, ARPU, conversion и hiring latency.

### 2.2 Output summary

| Метрика | p10 | p50 | p90 | Range width |
|---------|----:|----:|----:|------------:|
| EBITDA @M24, ₽/мес | -1 200 000 | 3 400 000 | 8 200 000 | 9 400 000 |
| CAC payback, мес | 6,3 | 3,0 | 2,5 | 3,8 |
| LTV/CAC | 2,0x | 9,7x | 15,0x | 13,0 |
| Cash runway, мес | 8 | 14,5 | 24 | 16 |

### 2.3 Интерпретация Monte Carlo Lite

- **Rule 1 срабатывает:** p10 EBITDA < 0, значит есть реальный сценарий неплатёжеспособности и это автоматически становится kill criterion #1.
- **Rule 2 проходит:** p50 EBITDA > 500k ₽/мес, значит median-case формально проходит EBITDA gate.
- **Rule 3 по сути срабатывает как downgrade:** распределение очень широкое, а нижний хвост уходит в отрицательную EBITDA. Даже если ratio p90/p10 некорректно считать из-за отрицательного p10, сама асимметрия означает высокую неопределённость.
- **Rule 4 срабатывает:** Range width по LTV/CAC = **13,0**, что заметно выше порога 8. Значит модель хрупкая прежде всего к сочетанию нестабильных CAC, pricing и churn.

Итог Monte Carlo Lite: кейс **ещё investable, но не robust**. Это не «спокойный compounder», а ставка на то, что Webiomed удержит enterprise pricing и не уйдёт в тяжёлый кастомный SI.

## 3. Competitor deep-dive

Ниже market-share estimates являются **инференсом**, а не официальной отчётностью: это rough share of visible category demand в соответствующем под-сегменте document / ambient / clinical AI по публичным внедрениям, медийному присутствию и продуктовой зрелости.

### 3.1 Западные конкуренты

| Компания | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **Nuance DAX Copilot** | Глубокая интеграция с Microsoft и EHR, enterprise security, сильный бренд в healthcare AI | Тяжёлый enterprise motion, высокая стоимость, слабая релевантность для РФ из-за data residency и санкционных ограничений | **25-30%** западного ambient/documentation AI enterprise-сегмента | Локальный data residency, ниже стоимость внедрения, лучше адаптация под РФ-регуляторику |
| **Abridge** | Сильная клиническая точность, Linked Evidence, хорошие позиции в Epic-centric workflow, сильный KLAS-сигнал | В первую очередь англоязычный/US workflow, высокая зависимость от зрелых EHR-контуров США | **20-25%** западного сегмента | Русскоязычный меддокумент workflow, локальные clinical rules и нормативка РФ |
| **Suki** | Быстрый voice/documentation workflow, ROI-ориентированный value prop, multi-assistant positioning | Меньше moat в clinical QA и compliance, чем у enterprise platform players; ориентир скорее на productivity, чем на жёсткий медаудит | **8-12%** западного сегмента | Для РФ-клиник Webiomed ближе к painkiller по качеству документации, а не просто к voice productivity tool |

### 3.2 Российские конкуренты

| Компания | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| **LazyDoc** | Сильный wedge в ambient documentation, понятный ROI по времени врача, SaaS/on-premise поставка | Уже ближе к scribe/voice layer, чем к deep clinical QA; меньше акцент на полном аудите карты и CDSS | **5-10%** локального сегмента | Webiomed глубже в clinical decision support, контроль качества ЭМК и B2B/B2G упаковку |
| **Medico Mind** | Чёткий painkiller: аудит карт, штрафы, Росздравнадзор, быстрый entry без сложной интеграции | Более лёгкая SaaS-модель может быть уязвима к commoditization и price pressure; слабее moat в крупных интеграциях | **3-5%** | Webiomed сильнее как enterprise platform и как продукт для крупных сетей/регионов |
| **Panacea Doc** | Фокус на качестве приёма, юррисках и контроле стандартов сервиса; сильный angle для owner/operator persona | Более ранняя стадия, меньше публичных доказательств масштаба, узкий workflow | **1-3%** | У Webiomed больше продуктовая ширина, зрелость и подтверждённая выручка |
| **iAmbulant** | Сильный сигнал на структурирование медкарт и инвестиционный интерес, технологический fit с digital records | Похоже на более ранний stage и более узкую специализацию на structured records | **2-4%** | Webiomed уже ближе к зрелому recurring B2B-продукту с revenue base и коммерческим контуром |
| **Собственные internal-модули МИС / интеграторов** | Дешевле для клиента на входе, быстрее procurement, уже стоят в контуре клиники | Обычно слабее по качеству моделей, explainability, continuous improvement и UI | **20-30% замещающей конкуренции** | Если Webiomed реально даёт measurable uplift по качеству и ROI, он может выиграть у «достаточно хороших» встроек |

### 3.3 Competitive takeaway

Главная угроза для Webiomed не в том, что западные лидеры завтра зайдут в РФ напрямую. Главная угроза в другом:
1. **локальные point-solutions** отъедят простые use-cases,
2. **МИС и интеграторы** встроят достаточно хороший document QA внутрь существующего контура,
3. pricing premium Webiomed начнёт сжиматься.

Поэтому defensibility должна строиться на трёх вещах: **регуляторная совместимость, доказуемый clinical ROI, глубокая интеграция в workflow клиники**.

## 4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Срыв найма CTO/ML/clinical roles | med | Высокий: roadmap и качество моделей тормозятся на 2-3 квартала | Time-to-hire > 3 мес, offer acceptance < 50% | Ранний pipeline найма, fractional experts, резерв на recruiter/search |
| Operational | Низкая repeatability интеграций с МИС | med | Высокий: проект превращается в SI, растут COGS и срок запуска | Внедрение > 8 недель, >30% задач кастомные | Стандартизировать коннекторы, ограничивать scope пилота, продавать пакет интеграции отдельно |
| Operational | Зависимость от внешних LLM/API | high | Высокий: рост cost/performance volatility, риск деградации SLA | Cost per analyzed chart растёт >25%, latency spikes, API incidents | Мульти-модельный стек, fallback на локальные/NLP пайплайны, лимиты usage на клиента |
| Market | Частные клиники не готовы платить enterprise ARPA 250k+ | med | Высокий: ARPU падает, payback удлиняется | Win-rate падает, дисконт >20% становится нормой | Чёткий ROI-калькулятор, сегментация по сетям 30-100 врачей, pricing tiers |
| Market | Price compression из-за point solutions | high | Высокий: contribution margin быстро сжимается | Конкуренты заходят с тарифом в 2-5k ₽ на врача или freemium pilot | Упор на enterprise bundle, compliance, reporting, интеграцию и measurable ROI |
| Market | Слабый спрос вне пилотов, низкий pilot-to-paid | med | Высокий: CAC удваивается | Pilot-to-paid < 10%, sales cycle > 9 мес | Жёсткая квалификация ICP, paid pilot, post-pilot ROI report как gate |
| Regulatory | Ужесточение требований 152-ФЗ и локализации медданных | med | Высокий: нужен redesign хранения и контуров доступа | Клиенты чаще требуют on-prem/private cloud, растёт число security questionnaires | Локальное хранение, on-prem/private cloud, DPA и ИБ-пакет из коробки |
| Regulatory | Трактовка продукта как MD/СаМD с новыми требованиями Росздравнадзора | med | Высокий: рост time-to-market и compliance costs | Юрэкспертиза/заказчики требуют дополнительные регистрационные документы | Разделять assistive vs diagnostic claims, product governance, отдельный compliance backlog |
| Regulatory | 115-ФЗ / AML friction у крупных медгрупп и госзаказчиков | low | Средний: замедление оплаты и onboarding контрагентов | Увеличение срока KYC/contracting, стопы платежей | Стандартизированный KYC-пакет, чистая contract structure, проверка контрагентов заранее |
| Financial | Cash runway сжимается до <9 мес до достижения product-market proof | high | Критический: риск down-round или insolvency | Burn > 5 млн ₽/мес, касса < 12 мес без роста pipeline | Raise раньше, stage-gated hiring, заморозка non-core найма |
| Financial | Ослабление рубля и рост USD-linked model costs | high | Средний/высокий: COGS растёт без возможности мгновенно поднять цену | Доля inference cost в COGS растёт >40% | Валютный buffer, рублёвые контракты с пересмотром, локальные модели как hedge |
| Financial | Инфляция зарплат и налоговая нагрузка съедают margin | med | Средний: fixed cost уезжает вверх | FOT растёт >20% YoY без сопоставимого роста ARR | Индексация pricing, часть функций на contractors, автоматизация ops |
| Black swan | Новые санкции режут доступ к SaaS/моделям/облакам | med | Критический: продукт может потерять ключевые компоненты | Vendor notices, проблемы с оплатами и доступом | Резервный стек, локальные провайдеры, переносимые пайплайны, no-single-vendor policy |
| Black swan | Масштабный сбой или отключение LLM-поставщика | med | Высокий: остановка сервиса и reputational hit | Частые 5xx, лимиты, деградация качества | Failover на альтернативные модели, manual queueing, SLA buffers |
| Black swan | Военная/политическая эскалация бьёт по бюджетам клиник | med | Высокий: freeze закупок и удлинение продаж | Заморозка CAPEX/OPEX, перенос пилотов, урезание digital budgets | Смещение на ROI-first сегменты, shorter contracts, больше private-clinic focus |

## 5. Kill conditions через 6 месяцев

1. **Median-case insolvency signal:** по обновлённой модели p10 EBITDA@M24 остаётся < 0 и cash runway < 9 месяцев. Продолжать нельзя, потому что downside уже не покрывается скоростью роста.
2. **Weak monetization:** фактический **ARPA < 175 000 ₽** или средний дисконт > 30% от целевой цены. Это означает, что pricing moat не держится.
3. **Weak retention / conversion:** одновременно **monthly churn > 5%** и **pilot-to-paid < 10%**. В этом состоянии LTV/CAC ломается и кейс превращается в дорогой пилотный сервис, а не в SaaS.

## 6. Bottom line

SECTION B скорее **снижает уверенность**, чем повышает её. В economics base-case кейс выглядит сильным, но stress-test показывает, что:
- pricing power критичен,
- churn и CAC не имеют большого запаса,
- uncertainty range слишком широк.

Итог: **PASS с риском даунгрейда при IC**, если команда не докажет в ближайшие 6 месяцев стабильный enterprise pricing, pilot-to-paid и предсказуемый runway.

## Sources
- [T1] 04-economics.md этого кейса: blended CAC 758k ₽, payback, funnel, hiring timeline.
- [T2] 04-economics.md этого кейса: ARPU 250k ₽, churn 2,5%, LTV/CAC 9,7x, runway 14,5 мес.
- [T3] ChartMogul churn benchmark: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- [T4] Section A этого файла: optimistic ARPA 260k ₽, pessimistic ARPA 230k ₽; для stress взят дополнительный price cut до 175k ₽.
- [T5] Microsoft Nuance DAX Copilot: https://www.microsoft.com/en-us/microsoft-cloud/healthcare/nuance-dax-copilot
- [T6] Abridge product page: https://www.abridge.com/product
- [T7] Suki homepage / resource hub: https://www.suki.ai/
- [T8] LazyDoc: https://lazydoc.ai/ ; CNews signal: https://www.cnews.ru/news/line/2026-01-30_dialogovyj_ii_dlya_zdravoohraneniya
- [T9] Medico Mind: https://medicomind.ru/for-owners ; pricing: https://medicomind.ru/pricing ; VC signal: https://vc.ru/ai/2745925-ii-kontrol-kachestva-i-audit-meditsinskoy-dokumentatsii-v-klinike-medico-mind
- [T10] Panacea Doc quality control: https://panaceadoc.ru/qualitycontrol ; РБК Companies: https://companies.rbc.ru/id/1247700522070-ooo-panatseya-dok/
- [T11] iAmbulant / Сколково: https://sk.ru/news/skolovskij-startap-iambulant-privlyok-investicii-na-razvitie-ii-platformy-dlya-strukturirovaniya-medkart/
- [T12] Webiomed / Skolkovo / Checko signals уже собраны в 01-evidence.md этого кейса.

<!-- P6B-DONE -->


---

# Файл: 06-verdict.md

[HEALTHCARE] Webiomed — APPROVED WITH NOTES: 71/100 | EBITDA base=4154К₽/мес через 24 мес | LTV/CAC=9,7x | Ключевое преимущество: regulated document QA + clinical workflow встраивается в ЭМК | Главный риск: price compression и project-heavy внедрение.

# Webiomed healthcare document AI v2 — 06-verdict
sector: HEALTHCARE
status: APPROVED WITH NOTES
score: 71/100
date: 2026-04-25
slug: webiomed-healthcare-document-ai-v2
repo_path: approved/webiomed-healthcare-document-ai-v2/verdict.md

## Итог
**Вердикт инвесткомитета: APPROVED WITH NOTES.**

Кейс проходит approval gate, потому что одновременно выполняются два условия:
1. **Normalized score = 71/100**, то есть выше порога 70.
2. **company_ebitda_potential_rub_month = 4 154 000 ₽/мес** достижима при **50 клиентах** и на горизонте **до 24 месяцев**, что проходит обязательный profitability gate.

Это не простой AI-wrapper, а regulated healthcare workflow с реальной локальной выручкой, понятным buyer motion и сильной unit economics. Но approval даётся с оговорками: рынок остаётся sales-led, pricing очень чувствителен, а enterprise rollout легко превращается в тяжёлый интеграционный сервис.

## Этапы 1-5
### Этап 1 — Intake
Исходный wedge: Webiomed продаёт клиникам и региональным медсистемам AI-слой для контроля качества медицинской документации, клинических подсказок и снижения ошибок в ЭМК без найма дополнительного ручного аудита.

### Этап 2 — Validation / Evidence
Фактическая валидация категории уже есть:
- продукт Webiomed.DocReviewer проверяет качество меддокументов и формирует отчёт за **5–15 секунд**;
- компания уже вышла в контур коммерческой медицины;
- по публичным источникам у ООО «К-Скай» была выручка **142,4 млн ₽** в 2024 году и **103,1 млн ₽** в 2025 году, то есть buyer в РФ уже платит не только за пилоты;
- наличие регистрационного удостоверения и внедрений в десятках регионов снижает регуляторный риск.

### Этап 3 — Demand
Demand-stage опирается на файл `02-demand.md`, потому что отдельный `03-demand.md` в кейсе отсутствует.
Публичный exact-search спрос низкий, но B2B/B2G budget line подтверждена:
- рынок AI в российской медицине оценён в **12 млрд ₽**;
- SAM по кейсу сходится в коридоре **1,21–1,32 млрд ₽**;
- buyer universe состоит из крупных частных сетей, диагностических групп и региональных цифровых контуров;
- willingness to pay подтверждена открытыми price anchors аналогов и реальной выручкой Webiomed.

### Этап 4 — Economics
Базовая экономика strong enough for IC:
- customer_ltv_rub = **7 320 000 ₽**
- CAC = **758 000 ₽**
- LTV/CAC = **9,7x**
- CAC payback = **3,0 мес по revenue / 4,1 мес по contribution**
- Gross Margin = **73,2%**
- contribution_margin_rub_month = **183 000 ₽/мес**
- fixed_costs_rub_month = **5 896 000 ₽/мес**
- startup_capital_to_bep_rub = **38 094 203 ₽**

### Этап 5 — Critic / Finance Risk
PnL проходит, но хвостовые риски значимы:
- base M12 EBITDA = **-791 610 ₽/мес**
- Monte Carlo Lite: **p10 EBITDA @M24 = -1,2 млн ₽/мес**, **p50 = 3,4 млн ₽/мес**, **p90 = 8,2 млн ₽/мес**
- наиболее опасные sensitivity-факторы: **price -30%** и **CAC x2**

## Оценка
Source tier balance: T1=1, T2=11, T3=2, weighted=1.93. Penalty applied: -5 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 21 | «LTV/CAC = 9,7x», «CAC Payback = 3,0 месяца», «Contribution Margin = 73,2%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 21 | «При 50 клиентах EBITDA > 500 000 ₽/мес достижима», base-case даёт «порядка 4,1–4,4 млн ₽ EBITDA/мес». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 15 | «SAM bottom-up = 1,2096 млрд ₽», но internal demand check вернул «LOW» и tier-balance даёт штраф -5. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 16 | «контроль качества меддокументов», «API», «регистрационное удостоверение» и интеграция в ЭМК создают moat выше среднего. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 14 | «p10 EBITDA < 0», есть риск «project-heavy delivery», санкции, 152-ФЗ и зависимость от внешних LLM/API. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 20 | «Партнёры / интеграторы МИС» дают лучший CAC, а ICP и named-target GTM уже явно сформулированы. |

**Сумма raw:** 107/150  
**Normalized score = round((107 × 100) / 150) = 71/100**

## 7-factor moat framework
| Фактор | Балл (0-3) | Почему |
|---|---:|---|
| Network effects | 1 | Каждый новый клиент почти не усиливает продукт для остальных напрямую. |
| Switching costs | 3 | Данные, интеграции в МИС/ЭМК, обучение врачей и внутренние quality-процессы делают замену болезненной. |
| Scale economies | 2 | Shared infra, compliance и model ops улучшаются с ростом, хотя integration still partly custom. |
| Proprietary data / model advantage | 2 | Есть доступ к медицинским документам и накопленной clinical логике, но публичного доказательства размера датасета мало. |
| Regulatory moat | 3 | Регуляторная упаковка, медконтур, регистрационное удостоверение и data residency дают серьёзный барьер входа. |
| Brand / distribution | 2 | Webiomed заметен в локальном healthtech-контуре, но не монополист. |
| Embedded workflow | 3 | Решение сидит прямо в процессе ведения ЭМК, аудита и clinical guidance. |

**Moat raw = 16/21**  
**Moat score = round((16 × 25) / 21) = 19/25**

Комментарий: формальный 7-factor score тянет на 19/25, но итоговый rubric score по критерию #4 снижен до **16/25**, потому что moat пока сильнее в regulated workflow, чем в company-exclusive data flywheel.

## Investment committee view
### Почему кейс прошёл
1. **Есть локальная монетизация и category proof в РФ.**
2. **Unit economics сильная даже с консервативным churn.**
3. **EBITDA gate выполняется** при <50 клиентах и горизонте до 24 месяцев.
4. **Регуляторика и интеграции** создают защиту лучше, чем у generic AI-сервисов.

### Почему кейс не получил чистый APPROVED
1. Exact-demand по поисковому следу низкий.
2. Monte Carlo даёт отрицательный p10.
3. Price compression и integration drag могут быстро ухудшить модель.

## Полный бизнес-процесс из 04-economics.md
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ на 1 нового клиента | Уровень автоматизации |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-листа клиник и сетей | SDR | hh/рынок, сайт клиники, CRM | 0,5 дня | 4 000 | средний |
| 2 | Outreach по email/телефону/партнёрам | SDR | amoCRM, телефония, почта | 10-14 дней | 18 000 | средний |
| 3 | Qualification call | SDR + AE | CRM, скрипты, Zoom/Meet | 3-5 дней | 14 000 | средний |
| 4 | Demo продукта и ROI-кейс | AE + CEO/BD | презентация, demo, калькулятор ROI | 5-7 дней | 22 000 | низкий |
| 5 | Scoping: МИС, юридические ограничения, ИБ, обезличивание данных | CTO + AE + clinical expert | чек-листы, API docs, security Q&A | 1-2 недели | 36 000 | низкий |
| 6 | Подготовка pilot proposal и коммерческого предложения | AE + CEO | шаблон КП, калькуляция, CRM | 3-5 дней | 21 000 | средний |
| 7 | Pilot / интеграция / подключение | CTO + backend + ML + CSM | API, sandbox, мониторинг | 3-6 недель | 96 000 | низкий |
| 8 | Review результатов пилота, закупочный комитет | AE + CEO + clinical champion | отчёт по качеству, ROI summary | 1-2 недели | 31 000 | низкий |
| 9 | Договор, DPA, ИБ/legal согласование | CEO + ops/legal | ЭДО, шаблоны договора | 2-4 недели | 29 000 | средний |
| 10 | Выставление счёта, onboarding, запуск recurring payment | ops + CSM + finance | CRM, 1С/ЭДО, банк | 3-5 дней | 18 000 | высокий |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 7 320 000 ₽ |
| CAC | 758 000 ₽ |
| LTV/CAC | 9,7x |
| CAC Payback | 3,0 мес revenue / 4,1 мес contribution |
| Gross Margin | 73,2% |
| contribution_margin_rub_month | 183 000 ₽/мес |
| fixed_costs_rub_month | 5 896 000 ₽/мес |
| Break-even clients | 33 |
| clients_to_500k_ebitda | 35 |
| clients_to_1m_ebitda | 38 |
| months_to_500k_ebitda | 15 |
| months_to_1m_ebitda | 16 |
| company_ebitda_rub_month base | 4 154 000 ₽/мес при 50 клиентах |
| company_ebitda_potential_rub_month | 4 154 000 ₽/мес |
| startup_capital_to_bep_rub | 38 094 203 ₽ |

## Команда
| Роль | Функция | FOT fully-loaded ₽/мес |
|---|---|---:|
| CEO | продажи top accounts, fundraising, legal, partnerships | 845 000 |
| CTO / Tech Lead | архитектура, ИБ, интеграции с МИС | 715 000 |
| Senior Backend #1 | API, backend, integrations | 520 000 |
| Senior Backend #2 | data pipelines, backend features | 520 000 |
| ML Engineer | NLP/LLM quality, extraction, evaluation | 650 000 |
| DevOps | infra, monitoring, CI/CD, security hardening | 455 000 |
| Frontend | кабинеты, UX для клиник, dashboards | 364 000 |
| SDR | pipeline generation, outreach | 234 000 |
| AE | demo, pilot, closing | 429 000 |
| Customer Success | onboarding, adoption, renewals | 299 000 |
| Clinical expert / методист 0.5 FTE | проверка правил, quality logic, методология | 195 000 |
| **Итого** |  | **5 226 000 ₽/мес** |

## GTM — 10 named targets
| # | Название | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | МЕДСИ | крупная сеть с 145 клиниками и высокой ценой врачебного часа, где ROI от контроля ЭМК и clinical guidance наиболее понятен | email decision-maker + warm intro через digital health ecosystem | 450 000 ₽/мес |
| 2 | ГК «Мать и дитя» | много стандартизированных амбулаторных сценариев и высокий риск ошибок в документации | конференция + direct outreach к меддиректору | 350 000 ₽/мес |
| 3 | «СМ-Клиника» | большой поток амбулаторных приёмов и зрелый private-clinic workflow | email COO / CIO + follow-up после отраслевого кейса | 320 000 ₽/мес |
| 4 | EMC | premium-сегмент, где стоимость времени врача и quality assurance особенно высоки | founder-led outreach + email CMO/CIO | 300 000 ₽/мес |
| 5 | «РЖД-Медицина» | распределённая сеть и централизованный контур качества, подходящий для annual license | партнёрство с интегратором / procurement intro | 500 000 ₽/мес |
| 6 | ГК «Эксперт» | диагностические и многопрофильные центры с болью в стандартизации медзаписей | email decision-maker + отраслевая конференция | 280 000 ₽/мес |
| 7 | «Скандинавия / АВА-ПЕТЕР» | зрелая частная сеть с цифровым контуром и высокой нагрузкой на документацию | direct email + warm intro через профильные ассоциации | 300 000 ₽/мес |
| 8 | «Будь Здоров» | федеральная сеть, где экономия ручного аудита и снижение дефектов карт имеют сетевой ROI | партнёрский канал + outbound ABM | 320 000 ₽/мес |
| 9 | MedSwiss | private-clinic buyer с повторяемым outpatient workflow и понятным quality KPI | email decision-maker + тематический вебинар | 220 000 ₽/мес |
| 10 | МИАЦ/Депздрав Татарстана | региональный цифровой контур с подтверждённым интересом к AI в медицине и масштабом для B2G пилота | тендерный мониторинг + региональная конференция + партнёрство | 600 000 ₽/мес |

## Top-3 risks
| Риск | Вероятность | Impact | Почему это top-3 |
|---|---|---|---|
| Price compression и уход в более дешёвые point-solutions | high | high | Stress-case «Price -30%» уводит EBITDA @M12 до **-2 883 573 ₽**, то есть pricing power критичен. |
| Project-heavy интеграции с МИС и service creep | medium-high | high | Внедрение >8 недель и рост кастома превращают продукт в SI и съедают margin. |
| evidence_quality_unverified и низкий source-tier balance | medium | medium-high | Weighted tier balance **1.93** означает слабую долю T1-доказательств по рынку и спросу. |

## Proof points для APPROVED
1. **Есть локальная выручка:** у ООО «К-Скай» зафиксирована выручка 103,1-142,5 млн ₽ по публичным источникам за 2024-2025 годы.
2. **Есть продуктовый workflow:** DocReviewer проверяет качество меддокументов и формирует отчёт за 5–15 секунд.
3. **Есть regulatory packaging:** регистрационное удостоверение и работа в медконтуре снижают barrier risk.
4. **Есть category expansion в РФ:** рядом появляются LazyDoc, Medico Mind, Panacea Doc и iAmbulant как подтверждение отдельного document-AI сегмента.
5. **Есть EBITDA gate:** даже conservative base-case приводит к EBITDA значительно выше 500k ₽/мес при 50 клиентах.

## Что доказать в ближайшие 6 месяцев
1. **Pilot-to-paid ≥ 20%** на private-clinic ICP.
2. **Floor-price не ниже 250 000 ₽/мес** без системных скидок >20%.
3. **Стандартизированный MIS connector**, чтобы go-live укладывался в 6-8 недель.
4. **2-3 новых reference logos** вне existing network и не только в госконтуре.

## Delta vs previous
P5 существенно усилил кейс благодаря рабочей unit economics. P6 добавил risk discount: M12 ещё отрицательный, p10 по Monte Carlo ниже нуля, поэтому финальный статус не чистый APPROVED, а **APPROVED WITH NOTES**.

## Финальный комитетский вывод
**APPROVED WITH NOTES.**

Это инвестируемый vertical AI-layer для regulated healthcare в РФ, если фонд готов работать с длинным sales cycle, интеграциями и compliance-heavy delivery. Не подходит как лёгкий self-serve SaaS, но подходит как infrastructure-grade healthcare workflow с сильным LTV/CAC и понятным profitability path.
