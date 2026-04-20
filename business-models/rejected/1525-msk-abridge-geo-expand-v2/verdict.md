[GEO-EXPAND] 1525 MSK Abridge GEO Expand v2 — REJECTED: 62/100 | EBITDA base=598К₽/мес через 24 мес | LTV/CAC=8,8x | Ключевое преимущество: enterprise on-prem wedge через МИС и compliance | Главный риск: спрос в РФ остаётся LOW и service-load съедает маржу.

# 06-verdict

sector: GEO-EXPAND

**Статус:** REJECTED
**Итоговый балл:** 62/100
**Дата:** 2026-04-20
**Case slug:** 1525-msk-abridge-geo-expand-v2

---

## Оценка
Source tier balance: T1=2, T2=19, T3=0, weighted=2.10. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 18 | «LTV/CAC = 8.8x», «Gross Margin = 50.0%», «Gross-profit payback 6.8 мес» дают рабочую экономику, но без большого safety margin. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | «EBITDA > 500 тыс. ₽/мес достижима в lean-mode уже около 34-36 клиентов» и `EBITDA @M24 p50 = 650 000 ₽/мес`, но base M12 ещё отрицательный. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 13 | «Итог по спросу в РФ: LOW», при этом `SAM РФ = 4,16-4,7 млрд ₽`; после tier penalty критерий остаётся только минимально приемлемым. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 10 | «Настоящее преимущество возможно только как enterprise ambient documentation layer + МИС integrations + secure deployment», но hard moat пока слабый. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | «это не clean SaaS, а управляемый GEO-EXPAND кейс с умеренным upside и высоким execution risk», плюс 152-ФЗ, adoption врачей и heavy integrations. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 18 | Есть 10 named targets, channel fit через private healthcare, но «до оплаты много ручного труда и trust-building», а CAC = 957 273 ₽. |

**Raw sum:** 93/150  
**Normalized score:** 62/100  
**Пороговое решение:** REJECTED, потому что score < 65. Формальный profit gate в lean-mode проходит, но запас прочности по спросу, moat и execution недостаточен для investment committee.

---

## Moat

### 7-factor moat framework
| # | Фактор | Балл (0-3) | Комментарий |
|---|--------|------------:|-------------|
| 1 | Network effects | 0 | Каждый новый клиент не улучшает продукт для остальных напрямую. |
| 2 | Switching costs | 2 | Интеграции с МИС, шаблоны и привычка врачей создают заметный switching cost после внедрения. |
| 3 | Scale economies | 1 | Стандартизация rollout и QA помогает, но service-load остаётся высоким. |
| 4 | Proprietary data / model advantage | 1 | Есть потенциальный clinical data flywheel, но публичного доказательства масштаба уникального датасета нет. |
| 5 | Regulatory moat | 2 | On-prem, data residency и 152-ФЗ помогают, но это скорее bar-to-entry, чем непроходимая лицензия. |
| 6 | Brand / distribution | 1 | Категория валидирована Abridge, но локальный бренд в РФ отсутствует. |
| 7 | Embedded workflow | 2 | При успешном запуске продукт встраивается глубоко в документацию врача и QA-контур. |

**Сумма 7 факторов:** 9/21  
**Moat score:** round((9 × 25) / 21) = **11/25**

Вывод: moat слабый. Ни network effects, ни сильного data moat, ни dominant distribution пока нет. Основной defensibility, это integration depth и compliance deployment, но этого недостаточно для уверенного approve.

---

## FULL business process from 04-economics.md

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

Вывод по процессу: это consultative healthcare B2B sale с длинным trust-building, интеграциями и пилотом 4-6 недель. Модель масштабируется только при жёсткой стандартизации delivery.

---

## Key metrics

| Метрика | Значение |
|---|---:|
| CAC | 957 273 ₽ |
| customer_ltv_rub | 8 400 000 ₽ |
| LTV/CAC | 8,8x |
| CAC Payback | 6,8 месяца по gross profit |
| GM | 50,0% |
| contribution_margin_rub_month | 122 000 ₽/клиент/мес |
| fixed_costs_rub_month | 5 842 000 ₽/мес steady-state; 3 550 000 ₽/мес lean-mode |
| Break-even | 48 клиентов steady-state; 30 клиентов lean-mode |
| startup_capital_to_bep_rub | 29 000 000 ₽ base; 55 000 000 ₽+ pessimistic |
| clients_to_500k_ebitda | 34 |
| months_to_500k_ebitda | 24 |
| clients_to_1m_ebitda | 40 |
| months_to_1m_ebitda | 24 |
| company_ebitda_rub_month | -713 496 ₽/мес в M12 base scenario |
| company_ebitda_potential_rub_month | 598 000 ₽/мес при 34 клиентах; 1 330 000 ₽/мес при 40 клиентах в lean-mode |

---

## Team table

| Роль | Функция | Кол-во | Fully-loaded, ₽/мес |
|---|---|---:|---:|
| CEO / founder | enterprise sales, partnerships, fundraising | 1 | 715 000 |
| CTO / tech lead | архитектура, security, platform | 1 | 676 000 |
| Backend engineer | product/API, integrations | 2 | 988 000 |
| ML / applied AI engineer | ASR/LLM quality, evals | 1 | 624 000 |
| Integrations / solutions engineer | МИС-мэппинг, внедрение | 1 | 429 000 |
| SDR | outbound pipeline | 2 | 390 000 |
| AE | demo, pilots, closing | 1 | 364 000 |
| CSM / implementation | onboarding, adoption | 1 | 286 000 |
| Clinical SME / QA | specialty templates, QA | 1 | 364 000 |
| Finance / ops | billing, docs, contracts | 0.5 | 156 000 |
| **Итого payroll** |  | **11.5** | **4 992 000 ₽/мес** |

---

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | МЕДСИ | Крупная частная сеть с высокой нагрузкой на врачебную документацию и явной digital function. | email decision-maker CIO/директору по цифровизации | 600 000 ₽/мес |
| 2 | MD Medical Group / Мать и дитя | Много амбулаторных приёмов и premium-patient mix, где экономия времени врача монетизируется лучше всего. | executive intro + конференция MedSoft | 700 000 ₽/мес |
| 3 | EMC | Высокий ARPU пациента и сильные требования к clinical UX и compliance. | email medical director + pilot в одной specialty-линии | 500 000 ₽/мес |
| 4 | СМ-Клиника | Большой поток амбулаторных визитов и типовые процессы, где легко измерять ROI на throughput врача. | outbound AE + demo для операционного директора | 450 000 ₽/мес |
| 5 | Медскан | Сетевая медицина с цифровой зрелостью и вероятной готовностью к rollout по филиалам. | партнёрство с МИС-интегратором | 450 000 ₽/мес |
| 6 | АО «Медицина» | Premium-клиника с жёсткими требованиями к качеству документации и data security. | founder-led outreach + clinical champion | 350 000 ₽/мес |
| 7 | Скандинавия / АВА-ПЕТЕР | Повторяющиеся амбулаторные сценарии и сильный бренд в частной медицине. | конференция + physician champion outreach | 400 000 ₽/мес |
| 8 | Будь Здоров | Масштабная частная сеть, где clinician-time saving прямо влияет на economics филиалов. | email decision-maker + отраслевой вебинар | 500 000 ₽/мес |
| 9 | Поликлиника.ру | Большой поток амбулаторных приёмов и потребность стандартизировать документацию между врачами. | outbound через COO / Head of Digital | 350 000 ₽/мес |
| 10 | Альфа-Центр Здоровья | Реалистичный buyer для mid-market rollout без сверхдлинного госцикла. | партнёрство с отраслевым интегратором + email | 300 000 ₽/мес |

Комментарий: named targets взяты из buyer-list в demand stage и соответствуют enterprise-only GTM для private healthcare. Это повышает realism, но не снимает проблему длинного sales cycle и pilot-heavy delivery.

---

## Top-3 risks

| Риск | Probability | Impact | Почему критично |
|---|---|---|---|
| Weak moat и commoditization | High | High | Moat score 11/25, локальные speech/documentation vendors уже есть, а category wedge легко схлопывается в voice commodity. |
| Низкий подтверждённый спрос в РФ | High | High | `DEMAND = LOW` по ключам `ambient clinical documentation` и `автоматизация протокола приема врача`; есть риск, что рынок ещё не budget-line. |
| Service-load и integrations burn | High | High | «интеграции с МИС, обучение врачей, QA и compliance быстро съедают маржу», а ранний heavy hiring ломает EBITDA. |

Дополнительно: риск `evidence_quality_unverified` не ставлю, потому что строка `Sources: T1=2, T2=19` присутствует, но качество базы всё равно смещено в T2.

---

## Delta vs previous

Предыдущий похожий артефакт `1229-msk-abridge-geo-expand-v2` завершился как early reject на P3 со score 0/100. Текущий rerun прошёл полный P5/P6 контур и показал, что economics в enterprise-lean режиме **могут** сходиться. Это поднимает оценку до **62/100**, но investment decision не меняет: кейс всё ещё не проходит из-за слабого локального спроса, слабого moat и тяжёлого execution profile.

---

## Proof points required for APPROVAL

1. Минимум 3-5 публично или semi-public подтверждённых российских внедрений ambient documentation в частных сетях.
2. Pilot-to-paid conversion не ниже 30% на первых 10 пилотах.
3. Фактический COGS не выше 160 000 ₽/клиент/мес при GM >= 50%.
4. ARPA не ниже 280 000 ₽/мес без системных скидок выше 20%.
5. Время внедрения с МИС не дольше 6 недель для типового контура.

---

## LTV Upside Calculator

Для перехода из REJECTED в NEAR-PASS / APPROVED кейсу нужны не только дополнительные клиенты, но и улучшение contribution-quality.

| Рычаг | Текущее значение | Цель | Эффект |
|---|---:|---:|---|
| ARPA / MRR на клиента | 280 000 ₽ | 330 000-360 000 ₽ | Даёт +50-80 тыс. ₽ gross profit на клиента и сокращает путь к 500k EBITDA. |
| COGS на клиента | 140 000 ₽ | <=120 000 ₽ | Повышает GM до 57-64% и поднимает contribution_margin_rub_month. |
| Annual churn | 20% | <=15% | Поднимает customer_ltv_rub до 11,2-12,3 млн ₽. |
| Fully-loaded CAC | 957 273 ₽ | <=700 000 ₽ | Увеличивает LTV/CAC к 12-16x и снижает cash burn на ранней фазе. |
| Fixed costs lean-mode | 3 550 000 ₽ | <=3 000 000 ₽ | Сдвигает EBITDA gate с 34 к 29-30 клиентам. |

Rule of thumb: если одновременно добиться `ARPA 330k`, `COGS 120k` и `CAC 700k`, то contribution на клиента вырастет до ~192k ₽/мес и 500k EBITDA станет достижимой уже примерно на 19-20 клиентах вместо 34.

---

## Финальный вывод инвесткомитета

Это не self-serve AI scribe, а тяжёлый enterprise healthcare operator с on-prem deployment, интеграциями в МИС и compliance-heavy delivery. Экономика в lean-mode формально проходит порог EBITDA, но инвестиционный комитет смотрит не только на формальный gate, а на margin of safety. Здесь он слабый: локальный спрос ещё не сформирован как budget-line, moat недостаточно защищён, а execution risk высок. Поэтому текущее решение, **REJECTED**, с рекомендацией вернуться только после появления сильных российских proof points.
