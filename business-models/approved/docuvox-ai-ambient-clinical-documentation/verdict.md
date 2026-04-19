# DocuVox AI, ambient clinical documentation
**Статус:** APPROVED WITH NOTES
**Итоговый балл:** 71/100
**Дата:** 2026-04-19
**Сектор:** HEALTHCARE
**Slug:** docuvox-ai-ambient-clinical-documentation

---

## Этап 1 — Описание кейса
DocuVox — healthcare AI-система для ambient clinical documentation: запись и транскрибация приёма, автозаполнение протокола, структурирование жалоб и назначений, подготовка черновика медзаписи и экспорт в медицинские контуры. Базовая гипотеза, это recurring B2B SaaS для частных клиник и сетей, где экономия времени врача и скорость оформления документации напрямую конвертируются в ROI.

## Этап 2 — Evidence
Первичный российский сигнал уже нетривиальный: на сайте заявлены 500+ врачей и 50 000+ обработанных приёмов, плюс хранение данных в РФ и соответствие ФЗ-152. Это подтверждает, что кейс не теоретический, а уже касается production-use в медицинском контуре.

## Этап 3 — Demand Validation
По прямому keyword-demand категория пока LOW-MEDIUM, но не reject. В кейсе есть сильная B2B-боль, крупный коммерческий сегмент частных клиник, публичные substitutes с pricing и согласованные TAM/SAM/SOM в РФ. Source tier balance = T1=4, T2=6, T3=3, weighted=2.08, поэтому к Market+Demand применён только умеренный штраф -2.

## Этап 4 — Unit Economics
Ключевые метрики:
- CAC: 290 880 ₽
- customer_ltv_rub: 7 431 543 ₽
- LTV/CAC: 24,4x
- CAC Payback: 1,39 месяца
- GM: 69,0%
- contribution_margin_rub_month: 144 900 ₽/клиент/мес
- fixed_costs_rub_month: 5 932 000 ₽/мес
- Break-even: 41 клиент
- startup_capital_to_bep_rub: 32 338 000 ₽

Economics strong: кейс проходит Profit Gate и сохраняет запас по клиентской марже даже при умеренном ухудшении CAC.

## Этап 5 — Финансовая модель и критика
Base scenario выходит на 52 активных клиента и 1 602 800 ₽ EBITDA/мес к M12. Sensitivity показывает, что главный стресс-фактор, это не CAC, а price compression: при снижении цены на 30% EBITDA уходит в -1 673 200 ₽/мес. Monte Carlo Lite даёт высокий разброс, поэтому комитет трактует кейс как high-variance vertical healthtech, а не как спокойный SaaS.

## Этап 6 — Финальный вердикт инвесткомитета
**Итог: APPROVED WITH NOTES, 71/100.**

Почему одобрено:
1. Реальный российский painkiller use case уже доказан не только теорией, но и продуктовым сигналом 500+ врачей.
2. Unit economics и путь к EBITDA выглядят fundable: base M12 уже выше 500K, а при 50 клиентах компания сохраняет EBITDA > 1,4 млн ₽/мес.
3. GTM в private healthcare реалистичен через pilot-to-rollout и конкретный список 10 named targets.

Топ-3 риска:
1. Doctor adoption и качество summary в реальном шуме кабинета.
2. Длинный pilot-to-paid и enterprise procurement.
3. Price compression до уровня speech commodity.

Что доказать дальше:
1. Pilot-to-paid conversion не ниже 40% на первых 10 пилотах.
2. Weekly active doctors не ниже 70% через 60 дней после go-live.
3. ARPA не ниже 180 000 ₽/мес без системных скидок >20%.

## История прохождения пайплайна
- 2026-04-19, Program 4: DEMAND = LOW-MEDIUM, но не reject.
- 2026-04-19, Program 5: PASS по unit economics, LTV/CAC = 24,4x.
- 2026-04-19, Program 6: high-variance critic, но EBITDA gate пройден.
- 2026-04-19, Program 7: APPROVED WITH NOTES, 71/100.

## Полный артефакт Program 7
Ниже сохранён полный verdict из pipeline.

---

[HEALTHCARE] DocuVox AI — APPROVED WITH NOTES: 71/100 | EBITDA base=1603К₽/мес через 12 мес | LTV/CAC=24,4x | Ключевое преимущество: локальный clinical workflow layer поверх ASR для клиник РФ | Главный риск: doctor adoption и длинный pilot-to-paid цикл.

# DocuVox AI, ambient clinical documentation

sector: HEALTHCARE

**Статус:** APPROVED WITH NOTES
**Итоговый балл:** 71/100
**Дата:** 2026-04-19
**Case slug:** docuvox-ai-ambient-clinical-documentation

---

## Оценка
Source tier balance: T1=4, T2=6, T3=3, weighted=2.08. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | «LTV/CAC = 24.4x», «CAC Payback = 1.39 мес», «Contribution Margin = 69.0%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 22 | «Base M12 EBITDA = 1 602 800 ₽/мес», «Break-even достигается... в M11», на 50 клиентах EBITDA > 1,4 млн ₽/мес. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 16 | «DEMAND = LOW-MEDIUM, но не reject», `Sources: T1=4, T2=6, T3=3`, после tier penalty рынок остаётся валидным через частные клиники РФ. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | «ценность DocuVox не в ASR как таковом, а в vertical workflow, шаблонах, compliance, экспорте в медконтур». |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 15 | «главный продуктовый риск» — качество в реальном шуме кабинета, плюс «закупочный цикл растягивается до 6+ месяцев». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 19 | «Blended CAC 291k ₽», «pilot-to-rollout», и список 10 реальных buyers уже сформирован в demand stage. |

**Raw sum:** 107/150  
**Normalized score:** 71/100  
**Пороговое решение:** APPROVED WITH NOTES, потому что score 70-74 и `company_ebitda_potential_rub_month` проходит порог 500K ₽/мес при 50 клиентах и в горизонте 24 месяцев.

---

## Moat

### 7-factor moat framework
| # | Фактор | Балл (0-3) | Комментарий |
|---|--------|------------:|-------------|
| 1 | Network effects | 0 | Каждый новый клиент не делает core-product лучше для остальных напрямую. |
| 2 | Switching costs | 2 | Шаблоны, интеграции и clinician adaptation создают заметный switching cost после внедрения. |
| 3 | Scale economies | 2 | С ростом клиентской базы дешевеют шаблоны, rollout и support playbooks. |
| 4 | Proprietary data / model advantage | 1 | Есть 50 000+ обработанных приёмов, но публично не доказан масштаб уникального датасета как hard moat. |
| 5 | Regulatory moat | 2 | Хранение данных в РФ и ФЗ-152 помогают, но это ещё не недостижимый лицензируемый барьер. |
| 6 | Brand / distribution | 1 | Есть ранний рыночный сигнал и 500+ врачей, но бренд пока не стал категорией. |
| 7 | Embedded workflow | 3 | Продукт встраивается в ежедневную документацию врача, а это глубокий workflow wedge. |

**Moat score:** round((11 × 25) / 21) = **13/25**

Вывод: moat средний, ближе к нижней границе investment-grade. Он строится на локальном compliance-контуре, workflow embedding и интеграции в медпроцесс, но пока слаб по network effects, brand dominance и доказанному data advantage.

---

## FULL business process from 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-листа клиник и ЛПР | SDR | CRM, hh.ru, 2ГИС, Excel | 1.5 ч | 1 500 | 70% |
| 2 | Первичный outreach по email/Telegram/телефону | SDR | CRM, телефония, email-sequences | 6 ч | 4 500 | 80% |
| 3 | Квалификация ответа и запись discovery | SDR | CRM, календарь, чек-лист ICP | 1.5 ч | 1 200 | 60% |
| 4 | Discovery-call: боль, объём врачей, текущий workflow | AE + CEO | Meet, CRM, ROI-template | 2 ч | 3 500 | 30% |
| 5 | Демо и расчёт экономического эффекта | AE + CTO | Demo-стенд, ROI-калькулятор | 3 ч | 7 000 | 40% |
| 6 | Проверка ИБ / ФЗ-152 / хранения данных в РФ | CTO | Security questionnaire, docs | 3 ч | 5 000 | 20% |
| 7 | Пилот: подключение шаблонов и сценариев | CSM + Backend | Admin panel, API, support desk | 12 ч | 18 000 | 50% |
| 8 | Сопровождение пилота и сбор метрик | CSM + ML Engineer | Dashboard, BI, QA | 6 ч | 9 000 | 45% |
| 9 | Юридическое согласование и закупка | CEO + юрист | Договор, ЭДО, procurement docs | 5 ч | 15 000 | 15% |
| 10 | Финальные переговоры и закрытие | AE + CEO | CRM, pricing sheet | 3 ч | 6 500 | 25% |
| 11 | Выставление счёта | Finance/Ops | 1С, ЭДО, CRM | 1 ч | 1 200 | 85% |
| 12 | Контроль оплаты и старт production-rollout | Finance/Ops + CSM | банк-клиент, CRM, onboarding | 0.5 ч | 700 | 80% |

---

## Key metrics

| Метрика | Значение |
|---|---:|
| CAC | 290 880 ₽ |
| customer_ltv_rub | 7 431 543 ₽ |
| LTV/CAC | 24,4x |
| CAC Payback | 1,39 месяца |
| GM | 69,0% |
| contribution_margin_rub_month | 144 900 ₽/клиент/мес |
| fixed_costs_rub_month | 5 932 000 ₽/мес |
| Break-even | 41 клиент |
| startup_capital_to_bep_rub | 32 338 000 ₽ |
| clients_to_500k_ebitda | 44 |
| months_to_500k_ebitda | 12 |
| clients_to_1m_ebitda | 48 |
| months_to_1m_ebitda | 12 |
| company_ebitda_rub_month | 1 602 800 ₽/мес в M12 base scenario |
| company_ebitda_potential_rub_month | 1 445 000 ₽/мес при 50 клиентах |

---

## Team table

| Роль | Функция | Кол-во | Зарплата за 1, ₽/мес | Итого, ₽/мес |
|---|---|---:|---:|---:|
| CEO | enterprise sales, partnerships, fundraising | 1 | 845 000 | 845 000 |
| CTO / Tech Lead | архитектура, безопасность, интеграции | 1 | 715 000 | 715 000 |
| Senior Backend | product/API, medical templates, integrations | 2 | 585 000 | 1 170 000 |
| ML Engineer | ASR/LLM quality, prompt/RAG, quality eval | 1 | 715 000 | 715 000 |
| DevOps | secure infra, monitoring, data residency | 1 | 455 000 | 455 000 |
| Frontend | physician UX, кабинеты, dashboards | 1 | 390 000 | 390 000 |
| SDR | outbound pipeline, lead qualification | 1 | 221 000 | 221 000 |
| AE | demo, пилоты, закрытие сделки | 1 | 416 000 | 416 000 |
| Customer Success | onboarding, adoption, expansion | 1 | 325 000 | 325 000 |
| **Итого payroll** |  | **10** |  | **5 252 000 ₽/мес** |

---

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | МЕДСИ | Крупная сеть с высокой нагрузкой на врачебную документацию и явным budget owner в private healthcare. | email decision-maker CIO/CMIO + партнёрство с медицинским ИТ-интегратором | 600 000 ₽/мес |
| 2 | Мать и дитя / MD Medical Group | Много амбулаторных приёмов и premium-сегмент, где ценится экономия времени врача и качество записи. | executive intro + конференция MedSoft | 700 000 ₽/мес |
| 3 | EMC | Платёжеспособный сегмент, международный уровень требований к UX и compliance, сильный fit для premium workflow-layer. | email medical director + пилот в одной specialty-линии | 500 000 ₽/мес |
| 4 | СМ-Клиника | Большая сеть частных клиник, где можно быстро показать ROI на throughput врача и скорости заполнения протокола. | outbound AE + demo для операционного директора | 450 000 ₽/мес |
| 5 | Медскан | Сетевая медицина с цифровой зрелостью и вероятной готовностью к rollout по филиалам. | партнёрство с ЭМК/МИС-поставщиком | 450 000 ₽/мес |
| 6 | Будь Здоров | Масштабная частная сеть, для которой clinician-time saving прямо влияет на unit economics филиалов. | email decision-maker + отраслевой вебинар | 500 000 ₽/мес |
| 7 | Скандинавия / АВА-ПЕТЕР | Сильный бренд и много повторяющихся приёмов, где важно ускорение записей и снижение edit burden. | конференция + physician champion outreach | 400 000 ₽/мес |
| 8 | Поликлиника.ру | Большой поток амбулаторных приёмов и потребность стандартизировать документацию между врачами. | outbound через COO / Head of Digital | 350 000 ₽/мес |
| 9 | Семейный доктор | Сеть с типовым амбулаторным workflow, где проще запустить pilot-to-rollout на 10-20 врачах. | email decision-maker + партнёрство с интегратором МИС | 300 000 ₽/мес |
| 10 | Ниармедик | Подходит для доказательства ROI в частной сети среднего масштаба без сверхдлинного госцикла. | founder-led outreach + пилот в одной локации | 250 000 ₽/мес |

Комментарий: цели подобраны из реального buyer-list в 02-demand.md и соответствуют каналу продаж pilot-to-rollout для частных клиник РФ.

---

## Top-3 risks

| Риск | Probability | Impact | Почему критично |
|---|---|---|---|
| Doctor adoption и качество summary в реальном шуме кабинета | Medium | High | Если weekly active doctors <70% или edit rate >25%, retention быстро ломается. |
| Длинный pilot-to-paid и enterprise procurement | High | High | В кейсе прямо отмечено, что «закупочный цикл растягивается до 6+ месяцев», а это бьёт по CAC и burn. |
| Price compression до уровня speech commodity | High | High | Sensitivity показывает: при `Price -30%` EBITDA @M12 = -1 673 200 ₽/мес. |

---

## Proof points required for APPROVAL

1. Не менее 10 платящих клиник с weekly active doctors >= 70% через 60 дней после go-live.
2. Pilot-to-paid conversion не ниже 40% на первых 10 пилотах.
3. Средний edit rate AI-note не выше 25% по ключевым specialty.
4. CAC не выше 350 000 ₽ при доле партнёрского канала не ниже 25%.
5. ARPA не ниже 180 000 ₽/мес без системных скидок больше 20%.

---

## Финальный вывод инвесткомитета

Это не search-led категория, а painkiller для частных клиник и сетей. Кейс проходит по unit economics и EBITDA уже в базовом сценарии, а качество евиденции достаточно сильное для investment committee за счёт сочетания T1/T2 источников и реального российского сигнала. Одобрение даётся **с замечаниями**: до следующего раунда нужно доказать doctor adoption, устойчивый pilot-to-paid conversion и удержание premium pricing.
