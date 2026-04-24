[HEALTHCARE] Third Opinion — APPROVED WITH NOTES: 71/100 | EBITDA base=953К₽/мес через 12 мес | LTV/CAC=29,5x | Ключевое преимущество: регуляторно готовый radiology workflow с внедрениями в 58 регионах | Главный риск: price compression и длинный enterprise sales cycle.

# Third Opinion radiology AI RU v2 — 06-verdict
sector: HEALTHCARE
status: APPROVED WITH NOTES
score: 71/100
date: 2026-04-24
slug: third-opinion-radiology-ai-ru-v2

## Итог
**Вердикт инвесткомитета: APPROVED WITH NOTES.**

Кейс проходит approval gate, потому что одновременно выполняются два условия:
1. **Normalized score = 71/100**, то есть выше порога 70.
2. **company_ebitda_potential_rub_month = 953 000 ₽/мес** достигается при **48-50 клиентах** и **до 24 месяцев**, что проходит обязательный profitability gate.

Это не лёгкий self-serve SaaS, а тяжёлый regulated healthtech infrastructure play. Инвестиционный тезис держится на уже доказанной категории, реальной локальной монетизации и сильной unit economics, но с оговорками по execution risk, тендерным лагам и хрупкости pricing mix.

## Этапы 1-5
### Этап 1 — Intake
Кейс пришёл как rerun/resurrect после обновления всей аналитической системы. Исходный тезис: российский vertical AI для лучевой диагностики с PACS/РИС-интеграциями, гос- и частным контуром продаж, evidence по 58 регионам, 10 000+ врачей и 10 млн+ исследований.

### Этап 2 — Validation / Evidence
Evidence подтверждает, что категория в РФ уже industrial-grade, а не пилотная:
- Минздрав указывает **6,4 млн исследований в месяц**, анализируемых ИИ, и экономию времени диагностики **30-40%**.
- У Third Opinion подтверждены **регистрационные удостоверения Росздравнадзора**, **29 госконтрактов**, выручка **133,1 млн ₽** за 2025 год и прибыль **7,28 млн ₽**.
- Поддерживающие сигналы по Celsus, Botkin.AI и AIРА Labs показывают, что рынок не держится на одном игроке.

### Этап 3 — Demand
Прямой search-led спрос по exact category низкий, но enterprise/gov WTP подтверждён лучше, чем у большинства healthcare AI кейсов:
- публичные ценовые якоря в РФ есть на уровне **300 тыс. ₽/год**, **50 тыс. ₽/мес** и **1 млн ₽+**;
- есть зрелый buyer universe: регионы, частные сети, диагностические сети, федеральные контуры;
- рынок живёт через budget line, KPI лучевой службы и procurement motion, а не через keyword search.

### Этап 4 — Economics
Base economics сильная:
- customer_ltv_rub = **29 610 000 ₽**
- CAC = **1 003 506 ₽**
- LTV/CAC = **29,5x**
- CAC payback = **4,9 мес по gross profit / 5,9 мес по contribution**
- Gross Margin = **68,3%**
- contribution_margin_rub_month = **171 000 ₽/мес**
- fixed_costs_rub_month = **7 597 000 ₽/мес**
- startup_capital_to_bep_rub = **26 200 000-28 165 575 ₽**

### Этап 5 — Critic / Finance Risk
Monte Carlo Lite подтверждает не collapse, а volatility:
- **p10 EBITDA @M24 = -1,2 млн ₽/мес**
- **p50 EBITDA @M24 = 1,1 млн ₽/мес**
- **p90 EBITDA @M24 = 8,4 млн ₽/мес**

Следовательно, median-case проходит, но хвостовой downside остаётся существенным. Это оправдывает approve только с оговорками.

## Оценка
Source tier balance: T1=3, T2=8, T3=1, weighted=2.17. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | «LTV/CAC = 29,5x», «CAC Payback = 4,9 мес», «Gross Margin = 68,3%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | «48 клиентов → 611 000 ₽/мес», «50 клиентов → 953 000 ₽/мес», break-even около M11-M12. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 16 | «ИИ уже анализирует более 6,4 млн исследований в месяц», но exact-demand endpoint по категории остаётся LOW. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 16 | «58 регионов», «10 000+ врачей», «29 госконтрактов», регудостоверения и PACS/РИС-интеграции дают реальный, но не монопольный moat. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 15 | Monte Carlo p10 EBITDA ниже нуля, есть зависимость от тендеров, интеграций, импортного compute и длительного цикла сделки. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 18 | CAC ~1,0 млн ₽ укладывается в enterprise healthtech, named-target GTM повторяет уже доказанный private + regional motion. |

**Сумма raw:** 107/150  
**Normalized score = round((107 × 100) / 150) = 71/100**

## 7-factor moat framework
| Фактор | Балл (0-3) | Почему |
|---|---:|---|
| Network effects | 1 | Каждый новый клиент незначительно улучшает продукт для остальных; это не marketplace и не data-network flywheel первого порядка. |
| Switching costs | 3 | PACS/РИС/МИС-интеграции, клинические протоколы, обучение врачей и compliance делают замену дорогой. |
| Scale economies | 2 | Compute и shared compliance амортизируются по мере роста базы, но implementation всё ещё partly custom. |
| Proprietary data / model advantage | 3 | 10 млн+ исследований и 10 000+ врачей создают заметный data advantage внутри РФ-контура. |
| Regulatory moat | 3 | Регистрационные удостоверения Росздравнадзора, госконтракты и закупочный fit формируют сильный entry barrier. |
| Brand / distribution | 2 | Сильный локальный бренд в нише, инвестиция МЕДСИ и присутствие в 58 регионах, но не доминирование на всем рынке. |
| Embedded workflow | 3 | Продукт встроен прямо в radiology workflow и влияет на throughput, triage и quality assurance. |

**Moat raw = 17/21**  
**Moat score = round((17 × 25) / 21) = 20/25**

Комментарий: формально moat по 7-factor ближе к 20/25, но в итоговой рубрике criterion #4 снижен до **16/25**, потому что рынок уже конкурентный, а часть преимущества пока category-level, а не company-exclusive.

## Investment committee view
### Почему кейс прошёл
1. **Категория уже оплачивается в РФ**, а не существует только как пилот.
2. **Unit economics fund-level**, особенно по LTV/CAC и payback.
3. **EBITDA 500k+ достижима** при клиентской базе <50 и на горизонте до 24 месяцев.
4. **Регуляторный и интеграционный контур** создаёт защиту лучше, чем у generic AI products.

### Почему кейс не получил чистый APPROVED
1. Market demand по exact search остаётся слабым.
2. Tail-risk в Monte Carlo сохраняет отрицательный p10.
3. Есть риск, что часть рынка уйдёт в ценовое давление и project-heavy delivery.

## Полный бизнес-процесс из 04-economics.md
| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation |
|---|---|---|---|---|---:|---|
| 1 | Захват лида из вебинара/события/реферала | Marketing manager | сайт, вебинар-платформа, CRM | 0,5 ч | 1 500 | высокая |
| 2 | Первичный qualification call | SDR | amoCRM/Bitrix24, телефония | 1 ч | 2 500 | средняя |
| 3 | Discovery с главврачом/лучевой службой | AE + founder/medical expert | CRM, Zoom/Meet, deck | 2 ч | 12 000 | низкая |
| 4 | Сбор данных по потоку исследований и ИТ-ландшафту | Solutions engineer / CTO | checklist, PACS/РИС audit sheet | 4 ч | 18 000 | низкая |
| 5 | Demo и clinical value workshop | AE + medical expert | demo environment | 2 ч | 15 000 | низкая |
| 6 | Security/regulatory review | CTO + compliance | шаблоны ИБ, мед. документация | 1-2 недели | 35 000 | низкая |
| 7 | Пилот и настройка интеграции | ML + backend + integration engineer | API gateway, PACS/РИС connectors | 3-6 недель | 180 000 | низкая |
| 8 | Согласование KPI пилота | AE + customer champion | pilot success plan | 3 ч | 10 000 | средняя |
| 9 | Procurement / tender / договор | AE + legal + finance | ЭДО, тендерные площадки | 2-8 недель | 85 000 | низкая |
| 10 | Final pricing / approval | CEO + AE | pricing model, approval matrix | 2 ч | 8 000 | низкая |
| 11 | Счёт, закрывающие документы | Finance ops | 1С, Диадок | 2 ч | 4 000 | высокая |
| 12 | Оплата первого месяца / аванса | Customer AP + finance ops | банк, ЭДО | 5-20 раб. дней | 2 000 | средняя |
| 13 | Go-live и обучение врачей | CSM + medical expert | LMS, knowledge base | 1-2 недели | 55 000 | средняя |
| 14 | Ежемесячный usage review / SLA / renewal base | CSM + support | BI dashboard, ticketing | 3 ч/мес | 12 000/мес | средняя |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 29 610 000 ₽ |
| CAC | 1 003 506 ₽ |
| LTV/CAC | 29,5x |
| CAC Payback | 4,9 мес gross / 5,9 мес contribution |
| Gross Margin | 68,3% |
| contribution_margin_rub_month | 171 000 ₽/мес |
| fixed_costs_rub_month | 7 597 000 ₽/мес |
| Break-even clients | 44,4 |
| clients_to_500k_ebitda | 48 |
| clients_to_1m_ebitda | 48-50 |
| months_to_500k_ebitda | 11-12 |
| months_to_1m_ebitda | 12 |
| company_ebitda_rub_month base | 953 000 ₽/мес при 50 клиентах |
| company_ebitda_potential_rub_month | 953 000 ₽/мес |
| startup_capital_to_bep_rub | 28 165 575 ₽ |

## Команда
| Роль | Функция | FOT fully-loaded ₽/мес |
|---|---|---:|
| CEO | продажи top-tier, fundraising, ключевые партнёры | 845 000 |
| CTO/Tech Lead | архитектура, безопасность, интеграции, релизы | 715 000 |
| Senior Backend #1 | API, integration layer, PACS/РИС connectors | 546 000 |
| Senior Backend #2 | data pipeline, billing, admin, SLA tooling | 546 000 |
| ML Engineer #1 | inference pipeline, quality metrics, retraining | 650 000 |
| ML Engineer #2 | clinical QA, model ops, new modalities | 650 000 |
| DevOps | infra, observability, uptime, perimeters | 455 000 |
| Frontend | physician UI, admin console, reporting | 390 000 |
| SDR | outbound prospecting, meetings, qualification | 221 000 |
| AE | discovery, pilots, procurement, close | 468 000 |
| Customer Success | onboarding, adoption, renewals | 325 000 |
| Product/Compliance | roadmap, docs, med device/QMS coordination | 416 000 |
| **Итого** |  | **6 227 000 ₽/мес** |

## GTM — 10 named targets
| # | Название | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | МЕДСИ | уже инвестировали в «Третье Мнение», сильный private-network fit и imaging volume | email decision-maker + warm intro через текущий cap table | 1 200 000 ₽/мес |
| 2 | Мать и дитя / MD Medical | большая сеть с маммографией и высокими требованиями к quality screening | conference + founder-led intro к medical director | 800 000 ₽/мес |
| 3 | EMC | premium сеть, готовность платить за speed + quality + second opinion workflow | direct email CMO/CIO | 700 000 ₽/мес |
| 4 | РЖД-Медицина | распределённая сеть и централизованный digital contour, подходит multi-site модель | партнёрство + procurement intro | 900 000 ₽/мес |
| 5 | СМ-Клиника | уже публикует AI pilots в radiology, buyer pain по нагрузке радиологов подтверждена | vc.ru / PR follow-up + direct outreach | 600 000 ₽/мес |
| 6 | Будь Здоров | рынок уже доказал value radiology AI внутри сети через кейсы Celsus | partner intro через imaging/KIS vendors | 650 000 ₽/мес |
| 7 | ГК Эксперт | сеть МРТ/КТ-центров, высокая интенсивность исследований и прямая боль в throughput | email decision-maker + отраслевая конференция | 750 000 ₽/мес |
| 8 | Департамент здравоохранения Москвы / Центр диагностики и телемедицины | крупнейший гос-контур AI imaging в РФ, сильный benchmark buyer | тендер + пилот через городской контур | 1 500 000 ₽/мес |
| 9 | Минздрав Московской области | регион с крупной инфраструктурой и цифровыми программами в диагностике | тендер / госпрограмма / отраслевой форум | 1 000 000 ₽/мес |
| 10 | Минздрав Республики Татарстан | сильный цифровой регион, вероятен interest в throughput и quality control radiology | conference + tender watch + local integrator partner | 900 000 ₽/мес |

## Top-3 risks
| Риск | Вероятность | Impact | Почему это top-3 |
|---|---|---|---|
| Price compression и уход в дешёвый single-site pricing | high | high | Экономика проходит только при enterprise/regional ACV; скидочный рынок быстро ломает EBITDA. |
| Integration drag и project-heavy delivery | medium | high | PACS/РИС-кастомизация может съесть margin и замедлить rollout новых клиентов. |
| Cash-flow / tender lag | medium-high | high | Длинные procurement cycles и ДЗ создают кассовый разрыв даже при хорошем LTV/CAC. |

## Proof points для APPROVED
1. **Есть реальная локальная выручка:** 133,1 млн ₽ в 2025 году у ООО «Платформа Третье Мнение».
2. **Есть regulated moat:** регистрационные удостоверения Росздравнадзора по продуктам.
3. **Есть масштаб коммерческого использования:** 58 регионов, 10 000+ врачей, 10 млн+ исследований.
4. **Есть частный и госканал одновременно:** МЕДСИ как private proof, 29 госконтрактов как public proof.
5. **Есть category maturity:** Минздрав публично подтверждает 6,4 млн AI-анализов в месяц в РФ.

## Что доказать в ближайшие 6 месяцев
1. Стабильный **pilot-to-paid conversion ≥ 30%** на новых enterprise/regional логотипах.
2. Blended ARPA не ниже **300 000 ₽/мес** без системных скидок выше 25%.
3. Не менее 2 новых референсных кейсов с **go-live < 90 дней**.
4. DSO и тендерный lag не размывают cash runway ниже 9 месяцев.

## Delta vs previous
Предыдущего полноценного P7 verdict для этого rerun-кейса не было. Относительно старого triage тезис усилился за счёт новых правил: fully-loaded CAC, formal moat framework, Monte Carlo Lite и tier-aware scoring. Главный вывод не изменился: это сильная healthcare infrastructure модель, но только в enterprise/regional варианте.

## Финальный комитетский вывод
**APPROVED WITH NOTES.**

Это инвестиционно пригодный кейс для фонда, который умеет работать с regulated B2B healthtech, длинным sales cycle и инфраструктурным GTM. Не подходит инвестору, который ищет вирусный или self-serve AI SaaS. Подходит инвестору, который верит в глубокие integration moats, гос/частный hybrid distribution и высокую ценность AI-layer в radiology throughput.
