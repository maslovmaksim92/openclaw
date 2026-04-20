[GEO-EXPAND] Norm AI — REJECTED: 57/100 | EBITDA base=3540К₽/мес через 24 мес | LTV/CAC=3.79x | Ключевое преимущество: enterprise-only compliance workflow для regulated buyers | Главный риск: слабый moat и длинный sales cycle в РФ.

# 06-verdict

sector: GEO-EXPAND

## Финальный вердикт
**REJECTED, 57/100.**

Причина отказа не в том, что экономика полностью сломана. Наоборот, enterprise-only модель даёт рабочие unit economics и потенциал `company_ebitda_potential_rub_month > 500 000 ₽/мес` при горизонте до 24 месяцев. Но для investable geo-expand кейса в РФ этого недостаточно: спрос локально слабый, moat слабый, regulatory/data-localization адаптация дорогая, а execution слишком founder-heavy. На уровне инвесткомитета это выглядит как **интересный продукт, но хрупкая инвестиционная ставка**.

Отдельно: исходный triage, который относил сигнал к supporting evidence для broader compliance thesis, по итогам полной переоценки выглядит **скорее корректным**, чем ошибочным. Standalone-case в РФ не дотягивает до approval.

## Оценка
Source tier balance: T1=10, T2=14, T3=2, weighted=2.31. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 19 | «LTV/CAC = 3.79x», «CAC Payback: 11.1 месяца», «Contribution Margin = 63.3%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 17 | «p50 EBITDA > 500k ₽/мес» и «при 50 клиентах ... ~3.54 млн ₽/мес», но M12 ещё «-1 784 600 ₽». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 16 | «Итог по спросу в РФ: LOW», но buyer universe = «1,053 организаций» и hh.ru даёт «49 вакансий». |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 8 | Сильнее workflow depth, слабее network effects и regulatory moat; «weak moat». |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 11 | В risk matrix прямо указано: «founder-heavy sales», «зависимость от внешних LLM/API», «152-ФЗ и data residency». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 14 | GTM enterprise-fit есть, но «скорость закрытия regulated deals» названа самой уязвимой частью модели. |

**Сумма raw:** 85/150  
**Normalized score = round((85 × 100) / 150) = 57/100.**

## 7-factor moat framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных. |
| Switching costs | 1 | Есть данные, workflow и security review, но пока без доказанного lock-in в РФ. |
| Scale economies | 1 | Compute и delivery частично масштабируются, но high-touch внедрение съедает эффект масштаба. |
| Proprietary data / model advantage | 1 | Есть domain positioning и determinations, но нет проверенного локального датасетного преимущества под РФ. |
| Regulatory moat | 0 | Regulatory wedge заявлен, но локальный T1-proof на обязательную аккредитацию/лицензию отсутствует. |
| Brand / distribution | 2 | На Западе бренд заметный, но в РФ brand pull слабый и demand endpoint = LOW. |
| Embedded workflow | 2 | Если внедрение прошло, продукт глубоко встраивается в approval/compliance workflow клиента. |

**Moat score = round((7 × 25) / 21) = 8/25.**  
Итог: **weak moat**.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 12 673 000 ₽ |
| contribution_margin_rub_month | 190 000 ₽ |
| CAC fully-loaded | 3 341 000 ₽ |
| LTV/CAC | 3.79x |
| CAC Payback | 11.1 мес |
| GM% | 63.3% |
| fixed_costs_rub_month | 5 964 600 ₽ |
| company_ebitda_rub_month (M12 base) | -1 784 600 ₽/мес |
| company_ebitda_potential_rub_month | 3 540 000 ₽/мес |
| clients_to_500k_ebitda | 35 |
| months_to_500k_ebitda | 24 |
| clients_to_1m_ebitda | 37 |
| months_to_1m_ebitda | 24 |
| Break-even | 32 клиента по EBITDA, 35 с буфером |
| startup_capital_to_bep_rub | 57 312 814 ₽ |

## Полный бизнес-процесс от лида до платежа

| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Automation |
|---|---|---|---|---:|---:|---|
| 1 | Сбор target-account list по банкам/страховщикам | SDR | hh/СПАРК/ручной desk research/CRM | 2 ч | 2 700 | частично автоматизировано |
| 2 | Холодный outreach и первичная квалификация | SDR | email, Telegram, CRM, sequences | 3 ч | 4 100 | частично автоматизировано |
| 3 | Intro call и pain discovery | AE | видеозвонок, CRM | 1.5 ч | 4 100 | вручную |
| 4 | Compliance use-case scoping | AE + CEO | Zoom/Meet, Notion, CRM | 2 ч | 8 000 | вручную |
| 5 | Технический пресейл и security/QA ответы | CTO + ML Engineer | docs, security questionnaire | 5 ч | 18 800 | вручную |
| 6 | Пилотное ТЗ и proposal | AE + CTO + CEO | proposal doc, pricing sheet | 4 ч | 16 100 | частично автоматизировано |
| 7 | Пилот / sandbox / private-cloud setup | Backend + ML + DevOps | Yandex Cloud / private infra | 24 ч | 58 900 | частично автоматизировано |
| 8 | Юридическое согласование и procurement | CEO + AE | договор, redlines, email | 6 ч | 19 700 | вручную |
| 9 | Онбординг, policy ingestion, настройка workflow | CSM + ML + Backend | KB, workflow builder, support desk | 16 ч | 40 200 | частично автоматизировано |
| 10 | Выставление счёта и получение оплаты | Finance/CEO | банк-клиент, ЭДО, CRM | 1 ч | 2 000 | частично автоматизировано |

## Команда

| Роль | Функция | Fully-loaded ₽/мес | Time-to-hire | Ramp |
|---|---|---:|---:|---:|
| CEO / Founder | продажи, enterprise deals, fundraising | 845 000 | 0 | 0 |
| CTO / Tech Lead | архитектура, security, пресейл | 715 000 | 2 мес | 2 мес |
| Senior Backend #1 | API, integrations | 546 000 | 1-2 мес | 1.5 мес |
| Senior Backend #2 | workflow engine, infra code | 546 000 | 1-2 мес | 1.5 мес |
| ML Engineer | policy modeling, evals, RAG | 650 000 | 2-3 мес | 2 мес |
| DevOps | private cloud, CI/CD, observability | 455 000 | 1-2 мес | 1 мес |
| Frontend | admin/workbench UI | 390 000 | 1 мес | 1 мес |
| SDR | outbound prospecting | 249 600 | 0.5-1 мес | 1 мес |
| AE | discovery, pilots, close | 468 000 | 1-2 мес | 3 мес |
| Customer Success | onboarding, retention | 312 000 | 1 мес | 1 мес |
| **Итого team FOT** |  | **5 176 600 ₽/мес** |  |  |

## GTM: 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбербанк | крупнейший regulated buyer с heavy approval/compliance workload | email decision-maker + отраслевые конференции | 350 000 ₽/мес |
| 2 | ВТБ | сложный контур marketing/legal approvals и security review | founder-led intro + партнёрство с SI | 350 000 ₽/мес |
| 3 | Газпромбанк | большой документооборот и high-value procurement контур | direct outreach в legal/compliance | 300 000 ₽/мес |
| 4 | Альфа-Банк | сильный digital marketing volume и внутренние policy checks | email + warm intro через legaltech events | 300 000 ₽/мес |
| 5 | Т-Банк | быстрые digital workflows, но строгий regulated perimeter | outbound ABM + founder demo | 300 000 ₽/мес |
| 6 | Совкомбанк | масштабный розничный банк с частыми disclosure/approval процессами | ABM + партнёрский канал | 250 000 ₽/мес |
| 7 | Банк ДОМ.РФ | меньше масштаба, но хороший pilot target для compliance automation | email decision-maker | 250 000 ₽/мес |
| 8 | Россельхозбанк | крупная regulated организация с legacy-heavy workflow | конференция + SI-партнёрство | 250 000 ₽/мес |
| 9 | АльфаСтрахование | страховой buyer с нормативной и продуктовой нагрузкой | warm outreach в compliance/risk | 250 000 ₽/мес |
| 10 | СберСтрахование | большой объём policy/disclosure и enterprise-grade security bar | executive intro + конференции | 250 000 ₽/мес |

**Вывод по GTM:** named-target база реальна и канал fit понятен, но motion остаётся дорогим enterprise ABM. Это не repeatable low-friction SaaS funnel.

## Top-3 risks

| Риск | Вероятность | Impact | Почему это критично |
|---|---|---|---|
| Weak moat | high | high | Moat score = 8/25, значит pricing pressure и копирование со стороны local incumbents реальны. |
| Founder-heavy sales + длинный enterprise cycle | high | high | В risk matrix прямо: «founder-heavy sales» и «скорость закрытия regulated deals» самая уязвимая часть модели. |
| Data residency / LLM dependency | high | high | 152-ФЗ, private-cloud требования и зависимость от внешних LLM/API могут тормозить пилоты и margin. |

## Финансовая интерпретация для инвесткомитета

1. **Сильная сторона**: unit economics выглядят инвестиционно приемлемо, если продукт продаётся как дорогой enterprise compliance workflow, а не как generic legal copilot.
2. **Слабая сторона**: локальный RU demand подтверждён больше buyer-universe и labor-cost proxy, чем реальным inbound/category pull.
3. **Почему reject при нормальной экономике**: фонд покупает не просто LTV/CAC, а repeatability + defensibility + scalable GTM. Здесь именно этих трёх элементов пока недостаточно.

## Что нужно доказать для пересмотра в APPROVED

1. **3-5 paid pilots в РФ** у банков/страховщиков с конверсией pilot-to-production не ниже 50%.
2. **Локальный moat**: private-cloud/on-prem deployment, audit trail и explainability, которые реально выигрывают procurement у Doczilla/Яндекса/generalist copilots.
3. **Сокращение founder dependency**: хотя бы 1 AE закрывает сделки без постоянного вовлечения CEO.
4. **Pricing proof**: удержание цены не ниже 300 000 ₽/мес без сильного pressure вниз.

## LTV Upside Calculator

### Базовый сценарий
- customer_ltv_rub = **12.67 млн ₽**
- CAC = **3.34 млн ₽**
- LTV/CAC = **3.79x**
- company_ebitda_rub_month potential = **3.54 млн ₽/мес** при 50 клиентах

### Что поднимет score к near-pass / approved
| Рычаг | Новое значение | Эффект |
|---|---:|---|
| ARPA | 350 000 ₽/мес | contribution_margin_rub_month вырастет до ~240 000 ₽ и ускорит EBITDA ramp |
| CAC | 2.5-2.8 млн ₽ | LTV/CAC уйдёт к ~4.5-5.0x |
| Monthly churn | 1.0% | customer_ltv_rub вырастет примерно до 19-24 млн ₽ в зависимости от COGS |
| Pilot-to-prod conversion | >50% | уменьшит founder burn и повысит GTM realism |
| Private-cloud reference cases | 2-3 клиента | повысит moat и снизит procurement friction |

### Условие re-open
Если одновременно будут достигнуты **ARPA ≥ 300k ₽**, **CAC ≤ 2.8 млн ₽**, **3 paid reference accounts** и **доказанный private-cloud procurement win**, кейс можно пересмотреть из REJECTED в NEAR-PASS/APPROVED WITH NOTES.

## Итог
Norm AI как продукт выглядит серьёзно, но **как standalone geo-expand инвестиция в РФ в 2026 году кейс пока преждевременный**. Для фонда это не "нет рынка", а "ещё не доказаны moat, локальная repeatability и de-risked GTM".
